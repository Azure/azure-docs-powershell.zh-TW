---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967542"
---
# <span data-ttu-id="77645-101">Remove-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="77645-101">Remove-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="77645-102">摘要</span><span class="sxs-lookup"><span data-stu-id="77645-102">SYNOPSIS</span></span>
<span data-ttu-id="77645-103">從服務設定中刪除存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="77645-103">Deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="77645-104">句法</span><span class="sxs-lookup"><span data-stu-id="77645-104">SYNTAX</span></span>

### <span data-ttu-id="77645-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="77645-105">IdentifyByName</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="77645-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="77645-106">IdentifyByObject</span></span>
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="77645-107">說明</span><span class="sxs-lookup"><span data-stu-id="77645-107">DESCRIPTION</span></span>
<span data-ttu-id="77645-108">**AzureStorSimpleAccessControlRecord** Cmdlet 會從服務設定中刪除存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="77645-108">The **Remove-AzureStorSimpleAccessControlRecord** cmdlet deletes an access control record from the service configuration.</span></span>

## <span data-ttu-id="77645-109">示例</span><span class="sxs-lookup"><span data-stu-id="77645-109">EXAMPLES</span></span>

### <span data-ttu-id="77645-110">範例1：移除 Access Controlaccess 控制項 recordaccess 控制項</span><span class="sxs-lookup"><span data-stu-id="77645-110">Example 1: Remove an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

<span data-ttu-id="77645-111">這個命令會刪除名為 Acr10 的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="77645-111">This command deletes the access control record named Acr10.</span></span>
<span data-ttu-id="77645-112">這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-112">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="77645-113">範例2：使用 pipelineAccess Controlaccess Controlaccess 控制項移除 Access Controlaccess 控制項記錄</span><span class="sxs-lookup"><span data-stu-id="77645-113">Example 2: Remove an Access Controlaccess control record by using the pipelineAccess Controlaccess controlaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

<span data-ttu-id="77645-114">這個命令會使用 **AzureStorSimpleAccessControlRecord** 取得名為 Acr10 的 **AccessControlRecord** ，然後使用管線運算子將該物件傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77645-114">This command uses the **Get-AzureStorSimpleAccessControlRecord** to get the **AccessControlRecord** named Acr10, and then passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="77645-115">命令會啟動移除 **AccessControlRecord** 物件的作業，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-115">The command starts the operation that removes the **AccessControlRecord** object, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="77645-116">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77645-116">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="77645-117">參數</span><span class="sxs-lookup"><span data-stu-id="77645-117">PARAMETERS</span></span>

### <span data-ttu-id="77645-118">-ACR</span><span class="sxs-lookup"><span data-stu-id="77645-118">-ACR</span></span>
<span data-ttu-id="77645-119">指定要刪除的 **AccessControlRecord** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-119">Specifies an **AccessControlRecord** object to delete.</span></span>
<span data-ttu-id="77645-120">若要取得 **AccessControlRecord** 物件，請使用 **AzureStorSimpleAccessControlRecord** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77645-120">To obtain an **AccessControlRecord** object, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77645-121">-ACRName</span><span class="sxs-lookup"><span data-stu-id="77645-121">-ACRName</span></span>
<span data-ttu-id="77645-122">指定要刪除的存取控制記錄名稱。</span><span class="sxs-lookup"><span data-stu-id="77645-122">Specifies a name of the access control record to delete.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77645-123">-Force</span><span class="sxs-lookup"><span data-stu-id="77645-123">-Force</span></span>
<span data-ttu-id="77645-124">表示此 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="77645-124">Indicates that this cmdlet does not prompt you for confirmation.</span></span>

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

### <span data-ttu-id="77645-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="77645-125">-Profile</span></span>
<span data-ttu-id="77645-126">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="77645-126">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="77645-127">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="77645-127">-WaitForComplete</span></span>
<span data-ttu-id="77645-128">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="77645-128">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="77645-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77645-129">CommonParameters</span></span>
<span data-ttu-id="77645-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="77645-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77645-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="77645-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77645-132">輸入</span><span class="sxs-lookup"><span data-stu-id="77645-132">INPUTS</span></span>

### <span data-ttu-id="77645-133">AccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="77645-133">AccessControlRecord</span></span>
<span data-ttu-id="77645-134">這個 Cmdlet 接受 **AccessControlRecord** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-134">This cmdlet accepts an **AccessControlRecord** object.</span></span>
<span data-ttu-id="77645-135">**AccessControlRecord** 物件包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="77645-135">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="77645-136">**GlobalId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="77645-136">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="77645-137">**InitiatorName** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="77645-137">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="77645-138">**InstanceId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="77645-138">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="77645-139">**名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="77645-139">**Name** ( **String** )</span></span> 
- <span data-ttu-id="77645-140">**OperationInProgress** ( **OperationInProgress** ) </span><span class="sxs-lookup"><span data-stu-id="77645-140">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="77645-141">**VolumeCount** ( **int** ) </span><span class="sxs-lookup"><span data-stu-id="77645-141">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="77645-142">輸出</span><span class="sxs-lookup"><span data-stu-id="77645-142">OUTPUTS</span></span>

### <span data-ttu-id="77645-143">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="77645-143">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="77645-144">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-144">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="77645-145">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="77645-145">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="77645-146">筆記</span><span class="sxs-lookup"><span data-stu-id="77645-146">NOTES</span></span>

## <span data-ttu-id="77645-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="77645-147">RELATED LINKS</span></span>

[<span data-ttu-id="77645-148">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="77645-148">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="77645-149">新-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="77645-149">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="77645-150">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="77645-150">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="77645-151">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="77645-151">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


