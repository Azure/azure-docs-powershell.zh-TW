---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 903738f1cb2e816ce18c9e5e3c9b01cf3d4baa9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456507"
---
# <span data-ttu-id="bbea7-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbea7-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="bbea7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbea7-102">SYNOPSIS</span></span>
<span data-ttu-id="bbea7-103">取得網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="bbea7-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbea7-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbea7-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbea7-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbea7-105">DESCRIPTION</span></span>
<span data-ttu-id="bbea7-106">**AzureRmNetworkSecurityRuleConfig** Cmdlet 會取得 Azure 網路安全性群組的網路安全規則配置。</span><span class="sxs-lookup"><span data-stu-id="bbea7-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="bbea7-107">示例</span><span class="sxs-lookup"><span data-stu-id="bbea7-107">EXAMPLES</span></span>

### <span data-ttu-id="bbea7-108">1：檢索網路安全規則 config</span><span class="sxs-lookup"><span data-stu-id="bbea7-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="bbea7-109">這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure network security 群組中，檢索名為 "AllowInternetOutBound" 的預設規則。</span><span class="sxs-lookup"><span data-stu-id="bbea7-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="bbea7-110">2：只使用名稱來檢索網路安全規則配置</span><span class="sxs-lookup"><span data-stu-id="bbea7-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="bbea7-111">這個命令會從資源群組 "rg1" 中名為 "nsg1" 的 Azure 網路安全性群組中，檢索名為 "rdp-tcp 規則" 的使用者定義規則</span><span class="sxs-lookup"><span data-stu-id="bbea7-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="bbea7-112">參數</span><span class="sxs-lookup"><span data-stu-id="bbea7-112">PARAMETERS</span></span>

### <span data-ttu-id="bbea7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbea7-113">-DefaultProfile</span></span>
<span data-ttu-id="bbea7-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbea7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbea7-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="bbea7-115">-DefaultRules</span></span>
<span data-ttu-id="bbea7-116">指示此 Cmdlet 是否會取得使用者建立的規則設定或預設規則設定。</span><span class="sxs-lookup"><span data-stu-id="bbea7-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="bbea7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbea7-117">-Name</span></span>
<span data-ttu-id="bbea7-118">指定要取得的網路安全規則配置名稱。</span><span class="sxs-lookup"><span data-stu-id="bbea7-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="bbea7-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bbea7-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="bbea7-120">指定包含要取得之網路安全性規則配置的 **NetworkSecurityGroup** 物件。</span><span class="sxs-lookup"><span data-stu-id="bbea7-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="bbea7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbea7-121">CommonParameters</span></span>
<span data-ttu-id="bbea7-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbea7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbea7-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbea7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbea7-124">輸入</span><span class="sxs-lookup"><span data-stu-id="bbea7-124">INPUTS</span></span>

### <span data-ttu-id="bbea7-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="bbea7-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="bbea7-126">形參 "NetworkSecurityGroup" 接受管線中 "PSNetworkSecurityGroup" 類型的值</span><span class="sxs-lookup"><span data-stu-id="bbea7-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="bbea7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="bbea7-127">OUTPUTS</span></span>

### <span data-ttu-id="bbea7-128">PSSecurityRule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bbea7-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="bbea7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="bbea7-129">NOTES</span></span>

## <span data-ttu-id="bbea7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbea7-130">RELATED LINKS</span></span>

[<span data-ttu-id="bbea7-131">附加 AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbea7-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bbea7-132">新-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbea7-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bbea7-133">移除-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbea7-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="bbea7-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="bbea7-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


