---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: f861c1589d6f35c9650f0c20800b577e1724d66b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789566"
---
# <span data-ttu-id="8eef5-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eef5-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8eef5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8eef5-102">SYNOPSIS</span></span>
<span data-ttu-id="8eef5-103">取得網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="8eef5-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8eef5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8eef5-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8eef5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8eef5-105">DESCRIPTION</span></span>
<span data-ttu-id="8eef5-106">**AzNetworkSecurityRuleConfig** Cmdlet 會取得 Azure 網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="8eef5-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="8eef5-107">示例</span><span class="sxs-lookup"><span data-stu-id="8eef5-107">EXAMPLES</span></span>

### <span data-ttu-id="8eef5-108">1：檢索網路安全規則 config</span><span class="sxs-lookup"><span data-stu-id="8eef5-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="8eef5-109">這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure network security 群組中，檢索名為 "AllowInternetOutBound" 的預設規則。</span><span class="sxs-lookup"><span data-stu-id="8eef5-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="8eef5-110">2：只使用名稱來檢索網路安全規則配置</span><span class="sxs-lookup"><span data-stu-id="8eef5-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="8eef5-111">這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure 網路安全性群組中，檢索名為 "rdp-tcp 規則" 的使用者定義規則</span><span class="sxs-lookup"><span data-stu-id="8eef5-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="8eef5-112">參數</span><span class="sxs-lookup"><span data-stu-id="8eef5-112">PARAMETERS</span></span>

### <span data-ttu-id="8eef5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eef5-113">-DefaultProfile</span></span>
<span data-ttu-id="8eef5-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8eef5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eef5-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="8eef5-115">-DefaultRules</span></span>
<span data-ttu-id="8eef5-116">指示此 Cmdlet 是否會取得使用者建立的規則設定或預設規則設定。</span><span class="sxs-lookup"><span data-stu-id="8eef5-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="8eef5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8eef5-117">-Name</span></span>
<span data-ttu-id="8eef5-118">指定要取得的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="8eef5-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8eef5-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8eef5-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8eef5-120">指定包含要取得之網路安全性規則配置的 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="8eef5-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8eef5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eef5-121">CommonParameters</span></span>
<span data-ttu-id="8eef5-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8eef5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eef5-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8eef5-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eef5-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8eef5-124">INPUTS</span></span>

### <span data-ttu-id="8eef5-125">PSNetworkSecurityGroup 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8eef5-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8eef5-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8eef5-126">OUTPUTS</span></span>

### <span data-ttu-id="8eef5-127">PSSecurityRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8eef5-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8eef5-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8eef5-128">NOTES</span></span>

## <span data-ttu-id="8eef5-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8eef5-129">RELATED LINKS</span></span>

[<span data-ttu-id="8eef5-130">附加 AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eef5-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8eef5-131">新-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eef5-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8eef5-132">移除-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eef5-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8eef5-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8eef5-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


