---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967582"
---
# <span data-ttu-id="90016-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="90016-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="90016-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90016-102">SYNOPSIS</span></span>
<span data-ttu-id="90016-103">移除從保留 IP 位址到 VM 或雲端服務的關聯。</span><span class="sxs-lookup"><span data-stu-id="90016-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="90016-104">句法</span><span class="sxs-lookup"><span data-stu-id="90016-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="90016-105">說明</span><span class="sxs-lookup"><span data-stu-id="90016-105">DESCRIPTION</span></span>
<span data-ttu-id="90016-106">AzureReservedIPAssociation Cmdlet 會將保留 IP 位址與虛擬機器 (VM) 或雲端服務 **取消** 與其解除。</span><span class="sxs-lookup"><span data-stu-id="90016-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="90016-107">當作業完成時，保留的 IP 位址是免費的，而 VM/VIP 會從 Azure 清點取得動態公用 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90016-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="90016-108">示例</span><span class="sxs-lookup"><span data-stu-id="90016-108">EXAMPLES</span></span>

### <span data-ttu-id="90016-109">範例1：移除保留 IP 關聯</span><span class="sxs-lookup"><span data-stu-id="90016-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="90016-110">這個命令會從名為 PipTestWestEurope 的服務解除名為 ResIp14 的保留 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90016-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="90016-111">系統會將新的動態 VIP 指派給 PipTestWestEurope。</span><span class="sxs-lookup"><span data-stu-id="90016-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="90016-112">參數</span><span class="sxs-lookup"><span data-stu-id="90016-112">PARAMETERS</span></span>

### <span data-ttu-id="90016-113">-Force</span><span class="sxs-lookup"><span data-stu-id="90016-113">-Force</span></span>
<span data-ttu-id="90016-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="90016-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="90016-115">在移除保留的 IP 關聯時，請使用此標誌來略過警告訊息。</span><span class="sxs-lookup"><span data-stu-id="90016-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="90016-116">-InformationAction</span></span>
<span data-ttu-id="90016-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="90016-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="90016-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="90016-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="90016-119">持續</span><span class="sxs-lookup"><span data-stu-id="90016-119">Continue</span></span>
- <span data-ttu-id="90016-120">理會</span><span class="sxs-lookup"><span data-stu-id="90016-120">Ignore</span></span>
- <span data-ttu-id="90016-121">看</span><span class="sxs-lookup"><span data-stu-id="90016-121">Inquire</span></span>
- <span data-ttu-id="90016-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="90016-122">SilentlyContinue</span></span>
- <span data-ttu-id="90016-123">停止</span><span class="sxs-lookup"><span data-stu-id="90016-123">Stop</span></span>
- <span data-ttu-id="90016-124">封存</span><span class="sxs-lookup"><span data-stu-id="90016-124">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90016-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="90016-125">-InformationVariable</span></span>
<span data-ttu-id="90016-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="90016-126">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90016-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="90016-127">-Profile</span></span>
<span data-ttu-id="90016-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="90016-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="90016-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="90016-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90016-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="90016-130">-ReservedIPName</span></span>
<span data-ttu-id="90016-131">指定保留 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="90016-131">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90016-132">-ServiceName</span></span>
<span data-ttu-id="90016-133">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="90016-133">Specifies the  name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-134">-槽</span><span class="sxs-lookup"><span data-stu-id="90016-134">-Slot</span></span>
<span data-ttu-id="90016-135">指定部署環境。</span><span class="sxs-lookup"><span data-stu-id="90016-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="90016-136">此參數可接受的值為： [生產]、[轉移]。</span><span class="sxs-lookup"><span data-stu-id="90016-136">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="90016-137">-VirtualIPName</span></span>
<span data-ttu-id="90016-138">指定要從中移除與服務或 VM 關聯的虛擬 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="90016-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90016-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90016-139">CommonParameters</span></span>
<span data-ttu-id="90016-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90016-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90016-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90016-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90016-142">輸入</span><span class="sxs-lookup"><span data-stu-id="90016-142">INPUTS</span></span>

## <span data-ttu-id="90016-143">輸出</span><span class="sxs-lookup"><span data-stu-id="90016-143">OUTPUTS</span></span>

### <span data-ttu-id="90016-144">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="90016-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="90016-145">筆記</span><span class="sxs-lookup"><span data-stu-id="90016-145">NOTES</span></span>

## <span data-ttu-id="90016-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="90016-146">RELATED LINKS</span></span>

[<span data-ttu-id="90016-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="90016-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


