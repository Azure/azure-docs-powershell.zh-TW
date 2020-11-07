---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 69974370-4542-4417-BD9D-3928EB005C31
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81d6e523978196a47b01d21aa8e857027b0b4f40
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967397"
---
# <span data-ttu-id="e7a4e-101">Set-AzureSubnet</span><span class="sxs-lookup"><span data-stu-id="e7a4e-101">Set-AzureSubnet</span></span>

## <span data-ttu-id="e7a4e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a4e-103">定義 Azure 虛擬機器的子網清單。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-103">Defines the subnet list for an Azure virtual machine.</span></span>

## <span data-ttu-id="e7a4e-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7a4e-104">SYNTAX</span></span>

```
Set-AzureSubnet [-SubnetNames] <String[]> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e7a4e-105">說明</span><span class="sxs-lookup"><span data-stu-id="e7a4e-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a4e-106">AzureSubnet Cmdlet 會設定虛擬機器 **設定** 的子網清單。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-106">The **Set-AzureSubnet** cmdlet sets the subnet list for a virtual machine configuration.</span></span>
<span data-ttu-id="e7a4e-107">使用 **New-add-azurevm** 來設定虛擬機器的子網。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-107">Use with **New-AzureVM** to set the subnets for a virtual machine.</span></span>

## <span data-ttu-id="e7a4e-108">示例</span><span class="sxs-lookup"><span data-stu-id="e7a4e-108">EXAMPLES</span></span>

### <span data-ttu-id="e7a4e-109">範例1：將子網新增至虛擬機器配置</span><span class="sxs-lookup"><span data-stu-id="e7a4e-109">Example 1: Add a subnet to a virtual machine configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine04" -ImageName $image -InstanceSize "Small" | Add-AzureProvisioningConfig -Windows -Password "password" | Set-AzureSubnet "PubSubnet","PrivSubnet" | New-AzureVM -ServiceName "ContosoService03"
```

<span data-ttu-id="e7a4e-110">這個命令會將子網新增至虛擬機器配置，然後建立名為 VirtualMachine04 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-110">This command adds a subnet to the virtual machine configuration, and then creates the virtual machine named VirtualMachine04.</span></span>

## <span data-ttu-id="e7a4e-111">參數</span><span class="sxs-lookup"><span data-stu-id="e7a4e-111">PARAMETERS</span></span>

### <span data-ttu-id="e7a4e-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e7a4e-112">-InformationAction</span></span>
<span data-ttu-id="e7a4e-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e7a4e-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e7a4e-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7a4e-115">持續</span><span class="sxs-lookup"><span data-stu-id="e7a4e-115">Continue</span></span>
- <span data-ttu-id="e7a4e-116">理會</span><span class="sxs-lookup"><span data-stu-id="e7a4e-116">Ignore</span></span>
- <span data-ttu-id="e7a4e-117">看</span><span class="sxs-lookup"><span data-stu-id="e7a4e-117">Inquire</span></span>
- <span data-ttu-id="e7a4e-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e7a4e-118">SilentlyContinue</span></span>
- <span data-ttu-id="e7a4e-119">停止</span><span class="sxs-lookup"><span data-stu-id="e7a4e-119">Stop</span></span>
- <span data-ttu-id="e7a4e-120">封存</span><span class="sxs-lookup"><span data-stu-id="e7a4e-120">Suspend</span></span>

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

### <span data-ttu-id="e7a4e-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e7a4e-121">-InformationVariable</span></span>
<span data-ttu-id="e7a4e-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e7a4e-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e7a4e-123">-Profile</span></span>
<span data-ttu-id="e7a4e-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e7a4e-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e7a4e-126">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="e7a4e-126">-SubnetNames</span></span>
<span data-ttu-id="e7a4e-127">指定包含子網名稱清單的陣列。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-127">Specifies an array that contains the list of subnet names.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a4e-128">-VM</span><span class="sxs-lookup"><span data-stu-id="e7a4e-128">-VM</span></span>
<span data-ttu-id="e7a4e-129">指定虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-129">Specifies the virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7a4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a4e-130">CommonParameters</span></span>
<span data-ttu-id="e7a4e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a4e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e7a4e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a4e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e7a4e-133">INPUTS</span></span>

## <span data-ttu-id="e7a4e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e7a4e-134">OUTPUTS</span></span>

## <span data-ttu-id="e7a4e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e7a4e-135">NOTES</span></span>

## <span data-ttu-id="e7a4e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7a4e-136">RELATED LINKS</span></span>

[<span data-ttu-id="e7a4e-137">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="e7a4e-137">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="e7a4e-138">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="e7a4e-138">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="e7a4e-139">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="e7a4e-139">Update-AzureVM</span></span>](./Update-AzureVM.md)


