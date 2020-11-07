---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71CFCA9D-198E-481A-BB85-159477F25322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c050ea91cc85a89702fb6cf62f05779db7155e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967304"
---
# <span data-ttu-id="6f840-101">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6f840-101">Set-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="6f840-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f840-102">SYNOPSIS</span></span>
<span data-ttu-id="6f840-103">更新存取控制記錄的 IQN。</span><span class="sxs-lookup"><span data-stu-id="6f840-103">Updates the IQN of an access control record.</span></span>

## <span data-ttu-id="6f840-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f840-104">SYNTAX</span></span>

```
Set-AzureStorSimpleAccessControlRecord -ACRName <String> -IQNInitiatorName <String> [-WaitForComplete]
 [-NewName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6f840-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f840-105">DESCRIPTION</span></span>
<span data-ttu-id="6f840-106">**AzureStorSimpleAccessControlRecord** Cmdlet 會更新現有存取控制記錄的 iSCSI 限定名稱 (IQN) 。</span><span class="sxs-lookup"><span data-stu-id="6f840-106">The **Set-AzureStorSimpleAccessControlRecord** cmdlet updates the iSCSI qualified name (IQN) of an existing access control record.</span></span>

## <span data-ttu-id="6f840-107">示例</span><span class="sxs-lookup"><span data-stu-id="6f840-107">EXAMPLES</span></span>

### <span data-ttu-id="6f840-108">範例1：更新存取控制記錄</span><span class="sxs-lookup"><span data-stu-id="6f840-108">Example 1: Update an access control record</span></span>
```
PS C:\>Set-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -IQNInitiatorName "IqnUpdated" -WaitForComplete
VERBOSE: ClientRequestId: e4766335-f302-40e0-93bf-fad7aa488ae6_PS
VERBOSE: ClientRequestId: cfdbbd67-6ba5-4238-b743-b88f604079b9_PS
VERBOSE: About to run a task to update your Access Control Record! 
VERBOSE: ClientRequestId: d5cf2793-0ab5-40ff-ab6f-43e21bc4c0a4_PS


JobId        : 89502523-52fc-4ce2-b2d4-cb8c6692fb60
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your update operation has completed successfully. 
VERBOSE: ClientRequestId: cbd47519-3a3c-4365-b097-0fb7551c48ee_PS
GlobalId            : 
InitiatorName       : IqnUpdated
InstanceId          : 9bcfbc83-e196-4688-9016-827f51515c24
Name                : Acr10
OperationInProgress : None
VolumeCount         : 0
```

<span data-ttu-id="6f840-109">這個命令會更新名為 IqnUpdated 的 iSCSI 啟動器的名為 Acr10 的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="6f840-109">This command updates the access control record named Acr10 for the iSCSI initiator named IqnUpdated.</span></span>
<span data-ttu-id="6f840-110">這個命令會指定 *WaitForComplete* 參數，因此命令會等到作業完成，然後傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f840-110">This command specifies the *WaitForComplete* parameter, and, therefore, the command waits until the operation is complete, and then returns a **TaskStatusInfo** object.</span></span>

## <span data-ttu-id="6f840-111">參數</span><span class="sxs-lookup"><span data-stu-id="6f840-111">PARAMETERS</span></span>

### <span data-ttu-id="6f840-112">-ACRName</span><span class="sxs-lookup"><span data-stu-id="6f840-112">-ACRName</span></span>
<span data-ttu-id="6f840-113">指定要修改之存取控制記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f840-113">Specifies a name of the access control record to modify.</span></span>

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

### <span data-ttu-id="6f840-114">-IQNInitiatorName</span><span class="sxs-lookup"><span data-stu-id="6f840-114">-IQNInitiatorName</span></span>
<span data-ttu-id="6f840-115">指定此 Cmdlet 提供其存取權的 iSCSI 啟動器的 IQN。</span><span class="sxs-lookup"><span data-stu-id="6f840-115">Specifies the IQN of the iSCSI initiator to which this cmdlet provides access for the volume.</span></span>

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

### <span data-ttu-id="6f840-116">-NewName</span><span class="sxs-lookup"><span data-stu-id="6f840-116">-NewName</span></span>
<span data-ttu-id="6f840-117">指定存取控制記錄的新名稱。</span><span class="sxs-lookup"><span data-stu-id="6f840-117">Specifies a new name for access control record.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f840-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6f840-118">-Profile</span></span>
<span data-ttu-id="6f840-119">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6f840-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6f840-120">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6f840-120">-WaitForComplete</span></span>
<span data-ttu-id="6f840-121">指示這個指令在將控制權傳回給 Windows PowerShell 主控台之前，請先等待該作業完成。</span><span class="sxs-lookup"><span data-stu-id="6f840-121">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="6f840-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f840-122">CommonParameters</span></span>
<span data-ttu-id="6f840-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f840-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f840-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f840-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f840-125">輸入</span><span class="sxs-lookup"><span data-stu-id="6f840-125">INPUTS</span></span>

### <span data-ttu-id="6f840-126">所有</span><span class="sxs-lookup"><span data-stu-id="6f840-126">None</span></span>

## <span data-ttu-id="6f840-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6f840-127">OUTPUTS</span></span>

### <span data-ttu-id="6f840-128">TaskStatusInfo, TaskResponse</span><span class="sxs-lookup"><span data-stu-id="6f840-128">TaskStatusInfo, TaskResponse</span></span>
<span data-ttu-id="6f840-129">如果您指定 *WaitForComplete* 參數，這個 Cmdlet 會傳回 **TaskStatusInfo** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f840-129">This cmdlet returns a **TaskStatusInfo** object if you specify the *WaitForComplete* parameter.</span></span>
<span data-ttu-id="6f840-130">如果您沒有指定該參數，則會傳回 **TaskResponse** 物件。</span><span class="sxs-lookup"><span data-stu-id="6f840-130">If you do not specify that parameter, it returns a **TaskResponse** object.</span></span>

## <span data-ttu-id="6f840-131">筆記</span><span class="sxs-lookup"><span data-stu-id="6f840-131">NOTES</span></span>

## <span data-ttu-id="6f840-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f840-132">RELATED LINKS</span></span>

[<span data-ttu-id="6f840-133">AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6f840-133">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6f840-134">新-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6f840-134">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6f840-135">移除-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6f840-135">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)


