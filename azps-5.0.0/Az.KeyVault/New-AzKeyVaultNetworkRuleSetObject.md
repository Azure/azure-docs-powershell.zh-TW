---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141658"
---
# <span data-ttu-id="acf2b-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="acf2b-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="acf2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acf2b-102">SYNOPSIS</span></span>
<span data-ttu-id="acf2b-103">建立代表網路規則設定的物件。</span><span class="sxs-lookup"><span data-stu-id="acf2b-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="acf2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="acf2b-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acf2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="acf2b-105">DESCRIPTION</span></span>
<span data-ttu-id="acf2b-106">建立代表建立電子倉庫時可使用之網路規則設定的物件。</span><span class="sxs-lookup"><span data-stu-id="acf2b-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="acf2b-107">示例</span><span class="sxs-lookup"><span data-stu-id="acf2b-107">EXAMPLES</span></span>

### <span data-ttu-id="acf2b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acf2b-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="acf2b-109">建立新的電子倉庫並指定網路規則，以允許從 $myNetworkResId 所識別的虛擬網路存取指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="acf2b-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="acf2b-110">參數</span><span class="sxs-lookup"><span data-stu-id="acf2b-110">PARAMETERS</span></span>

### <span data-ttu-id="acf2b-111">-略過</span><span class="sxs-lookup"><span data-stu-id="acf2b-111">-Bypass</span></span>
<span data-ttu-id="acf2b-112">指定 [繞過網路規則]。</span><span class="sxs-lookup"><span data-stu-id="acf2b-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="acf2b-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="acf2b-113">-DefaultAction</span></span>
<span data-ttu-id="acf2b-114">指定網路規則的預設動作。</span><span class="sxs-lookup"><span data-stu-id="acf2b-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="acf2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf2b-115">-DefaultProfile</span></span>
<span data-ttu-id="acf2b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acf2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf2b-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="acf2b-117">-IpAddressRange</span></span>
<span data-ttu-id="acf2b-118">指定允許的網路 IP 位址範圍（網路規則）。</span><span class="sxs-lookup"><span data-stu-id="acf2b-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="acf2b-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="acf2b-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="acf2b-120">指定網路規則的 [允許的虛擬網路資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="acf2b-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="acf2b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf2b-121">CommonParameters</span></span>
<span data-ttu-id="acf2b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acf2b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf2b-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acf2b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf2b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="acf2b-124">INPUTS</span></span>

### <span data-ttu-id="acf2b-125">所有</span><span class="sxs-lookup"><span data-stu-id="acf2b-125">None</span></span>

## <span data-ttu-id="acf2b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="acf2b-126">OUTPUTS</span></span>

### <span data-ttu-id="acf2b-127">PSKeyVaultNetworkRuleSet 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="acf2b-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="acf2b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="acf2b-128">NOTES</span></span>

## <span data-ttu-id="acf2b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf2b-129">RELATED LINKS</span></span>
