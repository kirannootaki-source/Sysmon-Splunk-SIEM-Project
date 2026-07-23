# Splunk SPL Queries

## 1. View All Sysmon Events
```spl
index=* source="WinEventLog:Microsoft-Windows-Sysmon/Operational"
```

## 2. Process Creation Events (Event ID 1)
```spl
index=* EventCode=1
```

## 3. File Creation Events (Event ID 11)
```spl
index=* EventCode=11
```

## 4. Registry Events (Event ID 13)
```spl
index=* EventCode=13
```

## 5. DNS Queries (Event ID 22)
```spl
index=* EventCode=22
```

## 6. Network Connections (Event ID 3)
```spl
index=* EventCode=3
```

## 7. Top 10 Executed Processes
```spl
index=* EventCode=1
| stats count by Image
| sort -count
| head 10
```

## 8. Top Users Creating Processes
```spl
index=* EventCode=1
| stats count by User
| sort -count
| head 10
```

## 9. Total Process Creation Events
```spl
index=* EventCode=1
| stats count
```

## 10. Top DNS Queries
```spl
index=* EventCode=22
| stats count by QueryName
| sort -count
| head 10
```