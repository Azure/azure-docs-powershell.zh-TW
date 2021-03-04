---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: c45df01f86abcd7a2f475b62b517765f3045cb10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916034"
---
# <span data-ttu-id="baeb3-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="baeb3-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="baeb3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="baeb3-102">SYNOPSIS</span></span>
<span data-ttu-id="baeb3-103">取得網路安全性群組的網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="baeb3-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="baeb3-104">語法</span><span class="sxs-lookup"><span data-stu-id="baeb3-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baeb3-105">描述</span><span class="sxs-lookup"><span data-stu-id="baeb3-105">DESCRIPTION</span></span>
<span data-ttu-id="baeb3-106">**Get-AzNetworkSecurityRuleConfig** Cmdlet 會取得 Azure 網路安全性群組的網路安全性規則組。</span><span class="sxs-lookup"><span data-stu-id="baeb3-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="baeb3-107">例子</span><span class="sxs-lookup"><span data-stu-id="baeb3-107">EXAMPLES</span></span>

### <span data-ttu-id="baeb3-108">1：正在取回網路安全性規則設定檔</span><span class="sxs-lookup"><span data-stu-id="baeb3-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="baeb3-109">此命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure 網路安全性群組中，從名稱為 "AllowInternetOutBound" 的預設規則</span><span class="sxs-lookup"><span data-stu-id="baeb3-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="baeb3-110">2：僅使用名稱來取回網路安全性規則設定檔</span><span class="sxs-lookup"><span data-stu-id="baeb3-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="baeb3-111">此命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure 網路安全性群組，從名為 "rdp-rule" 的使用者定義規則</span><span class="sxs-lookup"><span data-stu-id="baeb3-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="baeb3-112">參數</span><span class="sxs-lookup"><span data-stu-id="baeb3-112">PARAMETERS</span></span>

### <span data-ttu-id="baeb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baeb3-113">-DefaultProfile</span></span>
<span data-ttu-id="baeb3-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="baeb3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baeb3-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="baeb3-115">-DefaultRules</span></span>
<span data-ttu-id="baeb3-116">指出此 Cmdlet 是否獲得使用者建立的規則組式或預設規則組式。</span><span class="sxs-lookup"><span data-stu-id="baeb3-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baeb3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="baeb3-117">-Name</span></span>
<span data-ttu-id="baeb3-118">指定要取得之網路安全性規則組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="baeb3-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baeb3-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="baeb3-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="baeb3-120">指定包含要取得之網路安全性規則配置的 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="baeb3-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baeb3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baeb3-121">CommonParameters</span></span>
<span data-ttu-id="baeb3-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="baeb3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baeb3-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="baeb3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baeb3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="baeb3-124">INPUTS</span></span>

### <span data-ttu-id="baeb3-125">Microsoft.Azure.Commands.Network.models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="baeb3-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="baeb3-126">輸出</span><span class="sxs-lookup"><span data-stu-id="baeb3-126">OUTPUTS</span></span>

### <span data-ttu-id="baeb3-127">Microsoft.Azure.Commands.Network.models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="baeb3-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="baeb3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="baeb3-128">NOTES</span></span>

## <span data-ttu-id="baeb3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="baeb3-129">RELATED LINKS</span></span>

[<span data-ttu-id="baeb3-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="baeb3-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="baeb3-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="baeb3-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="baeb3-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="baeb3-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="baeb3-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="baeb3-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


