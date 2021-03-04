---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 5f63ee4d1c55211b13eb525a76547064e61cba48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914774"
---
# <span data-ttu-id="72b36-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="72b36-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="72b36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72b36-102">SYNOPSIS</span></span>
<span data-ttu-id="72b36-103">建立代表網路規則設定的物件。</span><span class="sxs-lookup"><span data-stu-id="72b36-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="72b36-104">語法</span><span class="sxs-lookup"><span data-stu-id="72b36-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b36-105">描述</span><span class="sxs-lookup"><span data-stu-id="72b36-105">DESCRIPTION</span></span>
<span data-ttu-id="72b36-106">建立代表網路規則設定的物件，以用於建立保存庫。</span><span class="sxs-lookup"><span data-stu-id="72b36-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="72b36-107">例子</span><span class="sxs-lookup"><span data-stu-id="72b36-107">EXAMPLES</span></span>

### <span data-ttu-id="72b36-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="72b36-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="72b36-109">建立新儲存庫並指定網路規則，以允許從由使用者識別的$myNetworkResId。</span><span class="sxs-lookup"><span data-stu-id="72b36-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="72b36-110">參數</span><span class="sxs-lookup"><span data-stu-id="72b36-110">PARAMETERS</span></span>

### <span data-ttu-id="72b36-111">-旁路</span><span class="sxs-lookup"><span data-stu-id="72b36-111">-Bypass</span></span>
<span data-ttu-id="72b36-112">指定忽略網路規則。</span><span class="sxs-lookup"><span data-stu-id="72b36-112">Specifies bypass of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b36-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="72b36-113">-DefaultAction</span></span>
<span data-ttu-id="72b36-114">指定網路規則的預設動作。</span><span class="sxs-lookup"><span data-stu-id="72b36-114">Specifies default action of network rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b36-115">-DefaultProfile</span></span>
<span data-ttu-id="72b36-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72b36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b36-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="72b36-117">-IpAddressRange</span></span>
<span data-ttu-id="72b36-118">指定網路規則的允許網路 IP 位址範圍。</span><span class="sxs-lookup"><span data-stu-id="72b36-118">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b36-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="72b36-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="72b36-120">指定網路規則的允許虛擬網路資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="72b36-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72b36-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b36-121">CommonParameters</span></span>
<span data-ttu-id="72b36-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72b36-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b36-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72b36-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b36-124">輸入</span><span class="sxs-lookup"><span data-stu-id="72b36-124">INPUTS</span></span>

### <span data-ttu-id="72b36-125">沒有</span><span class="sxs-lookup"><span data-stu-id="72b36-125">None</span></span>

## <span data-ttu-id="72b36-126">輸出</span><span class="sxs-lookup"><span data-stu-id="72b36-126">OUTPUTS</span></span>

### <span data-ttu-id="72b36-127">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="72b36-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="72b36-128">筆記</span><span class="sxs-lookup"><span data-stu-id="72b36-128">NOTES</span></span>

## <span data-ttu-id="72b36-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="72b36-129">RELATED LINKS</span></span>
