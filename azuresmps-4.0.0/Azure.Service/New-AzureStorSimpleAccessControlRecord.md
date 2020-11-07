---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: ED6CDEA3-0A5D-47E6-B9D7-47D1862212DF
online version: ''
schema: 2.0.0
ms.openlocfilehash: b907627200ec2463d997ebb4faa834e2821b1c7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967656"
---
# <span data-ttu-id="e1df8-101">New-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e1df8-101">New-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="e1df8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1df8-102">SYNOPSIS</span></span>
<span data-ttu-id="e1df8-103">建立存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="e1df8-103">Creates an access control record.</span></span>

## <span data-ttu-id="e1df8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1df8-104">SYNTAX</span></span>

```
New-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e1df8-105">說明</span><span class="sxs-lookup"><span data-stu-id="e1df8-105">DESCRIPTION</span></span>
<span data-ttu-id="e1df8-106">**新的-AzureStorSimpleAccessControlRecord** Cmdlet 會建立存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="e1df8-106">The **New-AzureStorSimpleAccessControlRecord** cmdlet creates an access control record.</span></span>
<span data-ttu-id="e1df8-107">您可以使用 **AccessControlRecord** 物件來設定卷。</span><span class="sxs-lookup"><span data-stu-id="e1df8-107">You can use an **AccessControlRecord** object to configure volumes.</span></span>

## <span data-ttu-id="e1df8-108">示例</span><span class="sxs-lookup"><span data-stu-id="e1df8-108">EXAMPLES</span></span>

### <span data-ttu-id="e1df8-109">範例1：建立 Access Controlaccess 控制項記錄，並等待 resultaccess 控制項</span><span class="sxs-lookup"><span data-stu-id="e1df8-109">Example 1: Create an Access Controlaccess control record and wait for the resultaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "Iqn10" -WaitForComplete
Error      : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
JobId      : 08719243-3a76-43a5-a88b-e5f2b63ed3d9
JobSteps   : {}
Result     : Succeeded
Status     : Completed
TaskResult : Succeeded
StatusCode : OK
RequestId  : e12362c2c06615108ba8436cf85fcd40
```

<span data-ttu-id="e1df8-110">這個命令會為名為 Iqn10 的 iSCSI 啟動器建立名為 Acr10 的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="e1df8-110">This command creates an access control record named Acr10 for the iSCSI initiator named Iqn10.</span></span>
<span data-ttu-id="e1df8-111">這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1df8-111">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

### <span data-ttu-id="e1df8-112">範例2：建立 Access Controlaccess 控制項 recordaccess 控制項</span><span class="sxs-lookup"><span data-stu-id="e1df8-112">Example 2: Create an Access Controlaccess control recordaccess control</span></span>
```
PS C:\>New-AzureStorSimpleAccessControlRecord -ACRName "Acr11" -IQNInitiatorName "Iqn11"
VERBOSE: The create job is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
2bd56fbb-4b95-4f2c-b99f-6321231a018d for tracking the job status
```

<span data-ttu-id="e1df8-113">這個命令會為名為 Iqn11 的 iSCSI 啟動器建立名為 Acr11 的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="e1df8-113">This command creates an access control record named Acr11 for the iSCSI initiator named Iqn11.</span></span>
<span data-ttu-id="e1df8-114">這個命令不會指定 *WaitForComplete* 參數，因此，命令會啟動工作，然後傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1df8-114">This command does not specify the *WaitForComplete* parameter, and, therefore, the command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="e1df8-115">若要查看任務的狀態，請使用 **AzureStorSimpleTask** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e1df8-115">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="e1df8-116">參數</span><span class="sxs-lookup"><span data-stu-id="e1df8-116">PARAMETERS</span></span>

### <span data-ttu-id="e1df8-117">-ACRName</span><span class="sxs-lookup"><span data-stu-id="e1df8-117">-ACRName</span></span>
<span data-ttu-id="e1df8-118">指定存取控制記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1df8-118">Specifies a name for the access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1df8-119">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="e1df8-119">-IQNInitiatorName</span></span>
<span data-ttu-id="e1df8-120">指定此 Cmdlet 提供其存取權的 iSCSI 啟動器 (IQN) 的 iSCSI 限定名稱。</span><span class="sxs-lookup"><span data-stu-id="e1df8-120">Specifies the iSCSI qualified name (IQN) of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IQN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1df8-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e1df8-121">-Profile</span></span>
<span data-ttu-id="e1df8-122">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e1df8-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="e1df8-123">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="e1df8-123">-WaitForComplete</span></span>
<span data-ttu-id="e1df8-124">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="e1df8-124">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="e1df8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1df8-125">CommonParameters</span></span>
<span data-ttu-id="e1df8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1df8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1df8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1df8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1df8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e1df8-128">INPUTS</span></span>

### <span data-ttu-id="e1df8-129">所有</span><span class="sxs-lookup"><span data-stu-id="e1df8-129">None</span></span>

## <span data-ttu-id="e1df8-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e1df8-130">OUTPUTS</span></span>

### <span data-ttu-id="e1df8-131">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="e1df8-131">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="e1df8-132">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1df8-132">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="e1df8-133">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="e1df8-133">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="e1df8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="e1df8-134">NOTES</span></span>

## <span data-ttu-id="e1df8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1df8-135">RELATED LINKS</span></span>

[<span data-ttu-id="e1df8-136">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e1df8-136">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e1df8-137">移除-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e1df8-137">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e1df8-138">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="e1df8-138">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="e1df8-139">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="e1df8-139">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


