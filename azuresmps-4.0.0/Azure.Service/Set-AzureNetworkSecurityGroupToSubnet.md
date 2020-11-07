---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A14F9105-1422-4073-96CF-E75CFC039E05
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7eaf1af2efe3f93f4e0a44d54e1f07ea52166942
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967275"
---
# <span data-ttu-id="31c83-101">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="31c83-101">Set-AzureNetworkSecurityGroupToSubnet</span></span>

## <span data-ttu-id="31c83-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31c83-102">SYNOPSIS</span></span>
<span data-ttu-id="31c83-103">將網路安全群組與子網建立關聯。</span><span class="sxs-lookup"><span data-stu-id="31c83-103">Associates a network security group to a subnet.</span></span>

## <span data-ttu-id="31c83-104">句法</span><span class="sxs-lookup"><span data-stu-id="31c83-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityGroupToSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String> [-Force]
 [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31c83-105">說明</span><span class="sxs-lookup"><span data-stu-id="31c83-105">DESCRIPTION</span></span>
<span data-ttu-id="31c83-106">**AzureNetworkSecurityGroupToSubnet** Cmdlet 會將 Azure 網路安全群組與子閘道聯。</span><span class="sxs-lookup"><span data-stu-id="31c83-106">The **Set-AzureNetworkSecurityGroupToSubnet** cmdlet associates an Azure network security group to a subnet.</span></span>

## <span data-ttu-id="31c83-107">示例</span><span class="sxs-lookup"><span data-stu-id="31c83-107">EXAMPLES</span></span>

## <span data-ttu-id="31c83-108">參數</span><span class="sxs-lookup"><span data-stu-id="31c83-108">PARAMETERS</span></span>

### <span data-ttu-id="31c83-109">-Force</span><span class="sxs-lookup"><span data-stu-id="31c83-109">-Force</span></span>
<span data-ttu-id="31c83-110">表示這個 Cmdlet 不會提示您確認從子網上移除先前的網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="31c83-110">Indicates that this cmdlet does not prompt you to confirm the removal of a previous network security group from the subnet.</span></span>

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

### <span data-ttu-id="31c83-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="31c83-111">-Name</span></span>
<span data-ttu-id="31c83-112">指定此 Cmdlet 與子網相關聯之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31c83-112">Specifies the name of the network security group that this cmdlet associates to a subnet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31c83-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31c83-113">-PassThru</span></span>
<span data-ttu-id="31c83-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="31c83-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="31c83-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="31c83-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31c83-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="31c83-116">-Profile</span></span>
<span data-ttu-id="31c83-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="31c83-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="31c83-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="31c83-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31c83-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="31c83-119">-SubnetName</span></span>
<span data-ttu-id="31c83-120">指定此 Cmdlet 要與網路安全群組相關聯之子網的名稱。</span><span class="sxs-lookup"><span data-stu-id="31c83-120">Specifies the name of a subnet to which this cmdlet associates a network security group.</span></span>

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

### <span data-ttu-id="31c83-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="31c83-121">-VirtualNetworkName</span></span>
<span data-ttu-id="31c83-122">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="31c83-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="31c83-123">這個 Cmdlet 會將網路安全性群組與此參數指定的虛擬網路中的子網建立關聯。</span><span class="sxs-lookup"><span data-stu-id="31c83-123">This cmdlet associates a network security group to a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="31c83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31c83-124">CommonParameters</span></span>
<span data-ttu-id="31c83-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31c83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31c83-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31c83-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31c83-127">輸入</span><span class="sxs-lookup"><span data-stu-id="31c83-127">INPUTS</span></span>

## <span data-ttu-id="31c83-128">輸出</span><span class="sxs-lookup"><span data-stu-id="31c83-128">OUTPUTS</span></span>

## <span data-ttu-id="31c83-129">筆記</span><span class="sxs-lookup"><span data-stu-id="31c83-129">NOTES</span></span>

## <span data-ttu-id="31c83-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="31c83-130">RELATED LINKS</span></span>

[<span data-ttu-id="31c83-131">AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="31c83-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="31c83-132">移除-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="31c83-132">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>](./Remove-AzureNetworkSecurityGroupFromSubnet.md)


