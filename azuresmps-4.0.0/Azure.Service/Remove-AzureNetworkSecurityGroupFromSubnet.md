---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BABA5142-541F-40C8-AFF5-20E4283BE147
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a718e2f675b4a5e204610a2d4f1fb1aac4c5478
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967596"
---
# <span data-ttu-id="d87d6-101">Remove-AzureNetworkSecurityGroupFromSubnet</span><span class="sxs-lookup"><span data-stu-id="d87d6-101">Remove-AzureNetworkSecurityGroupFromSubnet</span></span>

## <span data-ttu-id="d87d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d87d6-102">SYNOPSIS</span></span>
<span data-ttu-id="d87d6-103">從子網上 Dissociates 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d87d6-103">Dissociates a network security group from a subnet.</span></span>

## <span data-ttu-id="d87d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="d87d6-104">SYNTAX</span></span>

```
Remove-AzureNetworkSecurityGroupFromSubnet -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d87d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="d87d6-105">DESCRIPTION</span></span>
<span data-ttu-id="d87d6-106">**AzureNetworkSecurityGroupFromSubnet** Cmdlet dissociates 來自子網上的 Azure 網路安全性群組。</span><span class="sxs-lookup"><span data-stu-id="d87d6-106">The **Remove-AzureNetworkSecurityGroupFromSubnet** cmdlet dissociates an Azure network security group from a subnet.</span></span>

## <span data-ttu-id="d87d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="d87d6-107">EXAMPLES</span></span>

## <span data-ttu-id="d87d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="d87d6-108">PARAMETERS</span></span>

### <span data-ttu-id="d87d6-109">-Force</span><span class="sxs-lookup"><span data-stu-id="d87d6-109">-Force</span></span>
<span data-ttu-id="d87d6-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d87d6-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d87d6-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="d87d6-111">-Name</span></span>
<span data-ttu-id="d87d6-112">指定此 Cmdlet 從子網 dissociates 之網路安全性群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d87d6-112">Specifies the name of the network security group that this cmdlet dissociates from a subnet.</span></span>

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

### <span data-ttu-id="d87d6-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d87d6-113">-PassThru</span></span>
<span data-ttu-id="d87d6-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="d87d6-114">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d87d6-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d87d6-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d87d6-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d87d6-116">-Profile</span></span>
<span data-ttu-id="d87d6-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d87d6-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d87d6-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d87d6-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d87d6-119">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d87d6-119">-SubnetName</span></span>
<span data-ttu-id="d87d6-120">指定此 Cmdlet dissociates 網路安全性群組的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="d87d6-120">Specifies the name of a subnet from which this cmdlet dissociates a network security group.</span></span>

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

### <span data-ttu-id="d87d6-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="d87d6-121">-VirtualNetworkName</span></span>
<span data-ttu-id="d87d6-122">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="d87d6-122">Specifies the name of a virtual network.</span></span>
<span data-ttu-id="d87d6-123">這個 Cmdlet 會將網路安全性群組與此參數指定的虛擬網路中的子網解除與。</span><span class="sxs-lookup"><span data-stu-id="d87d6-123">This cmdlet disassociates a network security group from a subnet in the virtual network that this parameter specifies.</span></span>

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

### <span data-ttu-id="d87d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87d6-124">CommonParameters</span></span>
<span data-ttu-id="d87d6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d87d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87d6-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d87d6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87d6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d87d6-127">INPUTS</span></span>

## <span data-ttu-id="d87d6-128">輸出</span><span class="sxs-lookup"><span data-stu-id="d87d6-128">OUTPUTS</span></span>

## <span data-ttu-id="d87d6-129">筆記</span><span class="sxs-lookup"><span data-stu-id="d87d6-129">NOTES</span></span>

## <span data-ttu-id="d87d6-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="d87d6-130">RELATED LINKS</span></span>

[<span data-ttu-id="d87d6-131">AzureNetworkSecurityGroupForSubnet</span><span class="sxs-lookup"><span data-stu-id="d87d6-131">Get-AzureNetworkSecurityGroupForSubnet</span></span>](./Get-AzureNetworkSecurityGroupForSubnet.md)

[<span data-ttu-id="d87d6-132">Set-AzureNetworkSecurityGroupToSubnet</span><span class="sxs-lookup"><span data-stu-id="d87d6-132">Set-AzureNetworkSecurityGroupToSubnet</span></span>](./Set-AzureNetworkSecurityGroupToSubnet.md)


