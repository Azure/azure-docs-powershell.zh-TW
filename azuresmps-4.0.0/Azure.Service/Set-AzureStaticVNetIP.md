---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E54E4D16-DB2A-4626-B543-773C187B2E08
online version: ''
schema: 2.0.0
ms.openlocfilehash: d242418117b1bb576206f9ebb5fd568bd3e63cd1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967308"
---
# <span data-ttu-id="1c059-101">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="1c059-101">Set-AzureStaticVNetIP</span></span>

## <span data-ttu-id="1c059-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c059-102">SYNOPSIS</span></span>
<span data-ttu-id="1c059-103">設定虛擬機器物件的靜態 VNet IP 位址資訊。</span><span class="sxs-lookup"><span data-stu-id="1c059-103">Sets the static VNet IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="1c059-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c059-104">SYNTAX</span></span>

```
Set-AzureStaticVNetIP [-IPAddress] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1c059-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c059-105">DESCRIPTION</span></span>
<span data-ttu-id="1c059-106">**AzureStaticVNetIP** Cmdlet 會針對虛擬電腦物件設定靜態虛擬網路 (VNET) IP 位址資訊。</span><span class="sxs-lookup"><span data-stu-id="1c059-106">The **Set-AzureStaticVNetIP** cmdlet sets the static virtual network (VNet) IP address information for a virtual machine object.</span></span>

## <span data-ttu-id="1c059-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c059-107">EXAMPLES</span></span>

### <span data-ttu-id="1c059-108">範例1：設定與虛擬機器相關聯的虛擬網路 IP 位址</span><span class="sxs-lookup"><span data-stu-id="1c059-108">Example 1: Set the virtual network IP address associated with a virtual machine</span></span>
```
PS C:\> # Prerequisite: VNet has been set up with SubNet
          # Set-AzureVNetConfig -ConfigurationPath $vnetConfigPath;

          $vm = New-AzureVMConfig -Name $vmname -ImageName $img -InstanceSize $sz | Add-AzureProvisioningConfig -Windows -Password $pwd -AdminUsername $usr;
          $vm = Set-AzureSubNet -VM $vm -SubNetNames $sn;
          Set-AzureStaticVNetIP -IPAddress $ip -VM $vm;
          New-AzureVM -ServiceName $svc -VMs $vm -VNetName $vnetName -Location $loc;
```

<span data-ttu-id="1c059-109">第一個命令會設定虛擬網路的配置路徑。</span><span class="sxs-lookup"><span data-stu-id="1c059-109">The first command sets the configuration path for a virtual network.</span></span>

<span data-ttu-id="1c059-110">第二個命令會建立虛擬機器配置。</span><span class="sxs-lookup"><span data-stu-id="1c059-110">The second command creates a virtual machine configuration.</span></span>

<span data-ttu-id="1c059-111">第三個命令會設定虛擬機器的子網。</span><span class="sxs-lookup"><span data-stu-id="1c059-111">The third command sets the subnet for the virtual machine.</span></span>

<span data-ttu-id="1c059-112">第四個命令會設定虛擬機器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="1c059-112">The fourth command sets the IP address for the virtual machine.</span></span>

<span data-ttu-id="1c059-113">第五個命令會使用虛擬機器建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1c059-113">The fifth command creates a virtual machine using the virtual machine.</span></span>

## <span data-ttu-id="1c059-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c059-114">PARAMETERS</span></span>

### <span data-ttu-id="1c059-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1c059-115">-InformationAction</span></span>
<span data-ttu-id="1c059-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1c059-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1c059-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1c059-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1c059-118">持續</span><span class="sxs-lookup"><span data-stu-id="1c059-118">Continue</span></span>
- <span data-ttu-id="1c059-119">理會</span><span class="sxs-lookup"><span data-stu-id="1c059-119">Ignore</span></span>
- <span data-ttu-id="1c059-120">看</span><span class="sxs-lookup"><span data-stu-id="1c059-120">Inquire</span></span>
- <span data-ttu-id="1c059-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1c059-121">SilentlyContinue</span></span>
- <span data-ttu-id="1c059-122">停止</span><span class="sxs-lookup"><span data-stu-id="1c059-122">Stop</span></span>
- <span data-ttu-id="1c059-123">封存</span><span class="sxs-lookup"><span data-stu-id="1c059-123">Suspend</span></span>

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

### <span data-ttu-id="1c059-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1c059-124">-InformationVariable</span></span>
<span data-ttu-id="1c059-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1c059-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1c059-126">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="1c059-126">-IPAddress</span></span>
<span data-ttu-id="1c059-127">指定靜態 VNet IP 位址</span><span class="sxs-lookup"><span data-stu-id="1c059-127">Specifies the static VNet IP address</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c059-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1c059-128">-Profile</span></span>
<span data-ttu-id="1c059-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1c059-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1c059-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1c059-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1c059-131">-VM</span><span class="sxs-lookup"><span data-stu-id="1c059-131">-VM</span></span>
<span data-ttu-id="1c059-132">指定要設定靜態 VNet IP 位址的持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="1c059-132">Specifies a persistent virtual machine object for which to set the static VNet IP address.</span></span>

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

### <span data-ttu-id="1c059-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c059-133">CommonParameters</span></span>
<span data-ttu-id="1c059-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c059-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c059-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1c059-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c059-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1c059-136">INPUTS</span></span>

## <span data-ttu-id="1c059-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1c059-137">OUTPUTS</span></span>

## <span data-ttu-id="1c059-138">筆記</span><span class="sxs-lookup"><span data-stu-id="1c059-138">NOTES</span></span>

## <span data-ttu-id="1c059-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c059-139">RELATED LINKS</span></span>

[<span data-ttu-id="1c059-140">AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="1c059-140">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="1c059-141">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="1c059-141">Test-AzureStaticVNetIP</span></span>](./Test-AzureStaticVNetIP.md)


