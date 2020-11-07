---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 76826524-480F-458E-A996-A9DBACB8BA9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4aa220334c75d3e6832698ec10fbad71896473d2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967473"
---
# <span data-ttu-id="057c5-101">Start-AzureStorSimpleDeviceBackupJob</span><span class="sxs-lookup"><span data-stu-id="057c5-101">Start-AzureStorSimpleDeviceBackupJob</span></span>

## <span data-ttu-id="057c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="057c5-102">SYNOPSIS</span></span>
<span data-ttu-id="057c5-103">開始從現有的備份原則建立備份的新作業。</span><span class="sxs-lookup"><span data-stu-id="057c5-103">Starts a new job that creates a backup from an existing backup policy.</span></span>

## <span data-ttu-id="057c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="057c5-104">SYNTAX</span></span>

### <span data-ttu-id="057c5-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="057c5-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="057c5-106">BackupTypeGiven</span><span class="sxs-lookup"><span data-stu-id="057c5-106">BackupTypeGiven</span></span>
```
Start-AzureStorSimpleDeviceBackupJob -DeviceName <String> -BackupPolicyId <String> -BackupType <String>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="057c5-107">說明</span><span class="sxs-lookup"><span data-stu-id="057c5-107">DESCRIPTION</span></span>
<span data-ttu-id="057c5-108">**AzureStorSimpleDeviceBackupJob** Cmdlet 會啟動新作業，以從 StorSimple 裝置上的現有備份原則建立備份。</span><span class="sxs-lookup"><span data-stu-id="057c5-108">The **Start-AzureStorSimpleDeviceBackupJob** cmdlet starts a new job that creates a backup from an existing backup policy on a StorSimple device.</span></span>
<span data-ttu-id="057c5-109">根據預設，這個 Cmdlet 會建立本機快照備份。</span><span class="sxs-lookup"><span data-stu-id="057c5-109">By default, this cmdlet creates a local snapshot backup.</span></span>
<span data-ttu-id="057c5-110">若要建立雲端備份，請為 *BackupType* 參數指定 CloudSnapshot 的值。</span><span class="sxs-lookup"><span data-stu-id="057c5-110">To create a cloud backup, specify a value of CloudSnapshot for the *BackupType* parameter.</span></span>

## <span data-ttu-id="057c5-111">示例</span><span class="sxs-lookup"><span data-stu-id="057c5-111">EXAMPLES</span></span>

### <span data-ttu-id="057c5-112">範例1：建立本機快照備份</span><span class="sxs-lookup"><span data-stu-id="057c5-112">Example 1: Create a local snapshot backup</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f"
JobId                                                                StatusCode RequestId
-----                                                                ---------- ---------
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08                                 Accepted   456cf6bafd427103b71c07145e26d35c

VERBOSE: Your backup operation has been submitted for processing. Use commandlet "Get-AzureStorSimpleJob -JobId
fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08" to track status.
```

<span data-ttu-id="057c5-113">這個命令會針對指定的原則識別碼建立本機快照備份。</span><span class="sxs-lookup"><span data-stu-id="057c5-113">This command creates a local snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="057c5-114">這個命令會啟動作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="057c5-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="057c5-115">若要查看作業的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="057c5-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="057c5-116">範例2：建立雲端快照備份並等待完成</span><span class="sxs-lookup"><span data-stu-id="057c5-116">Example 2: Create a cloud snapshot backup and wait to finish</span></span>
```
PS C:\>Start-AzureStorSimpleDeviceBackupJob -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -BackupType CloudSnapshot -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : fb9acdca-ed6f-4b69-93f2-5c0bce0a1e08
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : f28ecf6cf75a7f128ca18e6ae14f9003
```

<span data-ttu-id="057c5-117">這個命令會針對指定的原則識別碼建立雲端快照備份。</span><span class="sxs-lookup"><span data-stu-id="057c5-117">This command creates a cloud snapshot backup for the specified policy ID.</span></span>
<span data-ttu-id="057c5-118">這個命令會指定 *WaitForComplete* 參數，因此命令會完成任務，然後傳回作業的 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="057c5-118">This command specifies the *WaitForComplete* parameter, so the command completes the task, and then returns a **TaskStatusInfo** object for the job.</span></span>

## <span data-ttu-id="057c5-119">參數</span><span class="sxs-lookup"><span data-stu-id="057c5-119">PARAMETERS</span></span>

### <span data-ttu-id="057c5-120">-BackupPolicyId</span><span class="sxs-lookup"><span data-stu-id="057c5-120">-BackupPolicyId</span></span>
<span data-ttu-id="057c5-121">指定要用來建立備份的備份原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="057c5-121">Specifies the ID of the backup policy to use to create the backup.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057c5-122">-BackupType</span><span class="sxs-lookup"><span data-stu-id="057c5-122">-BackupType</span></span>
<span data-ttu-id="057c5-123">指定備份類型。</span><span class="sxs-lookup"><span data-stu-id="057c5-123">Specifies the backup type.</span></span>
<span data-ttu-id="057c5-124">有效值為： LocalSnapshot 和 CloudSnapshot。</span><span class="sxs-lookup"><span data-stu-id="057c5-124">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: BackupTypeGiven
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057c5-125">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="057c5-125">-DeviceName</span></span>
<span data-ttu-id="057c5-126">指定要在其上啟動備份作業的 StorSimple 裝置的名稱。</span><span class="sxs-lookup"><span data-stu-id="057c5-126">Specifies the name of the StorSimple device on which to start the backup job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057c5-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="057c5-127">-Profile</span></span>
<span data-ttu-id="057c5-128">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="057c5-128">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057c5-129">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="057c5-129">-WaitForComplete</span></span>
<span data-ttu-id="057c5-130">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="057c5-130">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="057c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="057c5-131">CommonParameters</span></span>
<span data-ttu-id="057c5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="057c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="057c5-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="057c5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="057c5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="057c5-134">INPUTS</span></span>

### <span data-ttu-id="057c5-135">所有</span><span class="sxs-lookup"><span data-stu-id="057c5-135">None</span></span>

## <span data-ttu-id="057c5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="057c5-136">OUTPUTS</span></span>

### <span data-ttu-id="057c5-137">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="057c5-137">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="057c5-138">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="057c5-138">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="057c5-139">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="057c5-139">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="057c5-140">筆記</span><span class="sxs-lookup"><span data-stu-id="057c5-140">NOTES</span></span>

## <span data-ttu-id="057c5-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="057c5-141">RELATED LINKS</span></span>

[<span data-ttu-id="057c5-142">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="057c5-142">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="057c5-143">開始-AzureStorSimpleDeviceBackupRestoreJob</span><span class="sxs-lookup"><span data-stu-id="057c5-143">Start-AzureStorSimpleDeviceBackupRestoreJob</span></span>](./Start-AzureStorSimpleDeviceBackupRestoreJob.md)


