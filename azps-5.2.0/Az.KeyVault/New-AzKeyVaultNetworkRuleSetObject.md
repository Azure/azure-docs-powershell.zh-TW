---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultnetworkrulesetobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultNetworkRuleSetObject.md
ms.openlocfilehash: 318d5915e07ac55430dbe8e1788d862673dc5998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277556"
---
# <span data-ttu-id="dd213-101">New-AzKeyVaultNetworkRuleSetObject</span><span class="sxs-lookup"><span data-stu-id="dd213-101">New-AzKeyVaultNetworkRuleSetObject</span></span>

## <span data-ttu-id="dd213-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd213-102">SYNOPSIS</span></span>
<span data-ttu-id="dd213-103">建立代表網路規則設定的物件。</span><span class="sxs-lookup"><span data-stu-id="dd213-103">Create an object representing the network rule settings.</span></span>

## <span data-ttu-id="dd213-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd213-104">SYNTAX</span></span>

```
New-AzKeyVaultNetworkRuleSetObject [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>]
 [-Bypass <PSKeyVaultNetworkRuleBypassEnum>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd213-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd213-105">DESCRIPTION</span></span>
<span data-ttu-id="dd213-106">建立代表建立電子倉庫時可使用之網路規則設定的物件。</span><span class="sxs-lookup"><span data-stu-id="dd213-106">Create an object representing the network rule settings that can be used when creating a vault.</span></span>

## <span data-ttu-id="dd213-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd213-107">EXAMPLES</span></span>

### <span data-ttu-id="dd213-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dd213-108">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="dd213-109">建立新的電子倉庫並指定網路規則，以允許從 $myNetworkResId 所識別的虛擬網路存取指定的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="dd213-109">Creating a new vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="dd213-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd213-110">PARAMETERS</span></span>

### <span data-ttu-id="dd213-111">-略過</span><span class="sxs-lookup"><span data-stu-id="dd213-111">-Bypass</span></span>
<span data-ttu-id="dd213-112">指定 [繞過網路規則]。</span><span class="sxs-lookup"><span data-stu-id="dd213-112">Specifies bypass of network rule.</span></span>

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

### <span data-ttu-id="dd213-113">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="dd213-113">-DefaultAction</span></span>
<span data-ttu-id="dd213-114">指定網路規則的預設動作。</span><span class="sxs-lookup"><span data-stu-id="dd213-114">Specifies default action of network rule.</span></span>

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

### <span data-ttu-id="dd213-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd213-115">-DefaultProfile</span></span>
<span data-ttu-id="dd213-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd213-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd213-117">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="dd213-117">-IpAddressRange</span></span>
<span data-ttu-id="dd213-118">指定允許的網路 IP 位址範圍（網路規則）。</span><span class="sxs-lookup"><span data-stu-id="dd213-118">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="dd213-119">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="dd213-119">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="dd213-120">指定網路規則的 [允許的虛擬網路資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="dd213-120">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="dd213-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd213-121">CommonParameters</span></span>
<span data-ttu-id="dd213-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd213-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd213-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dd213-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd213-124">輸入</span><span class="sxs-lookup"><span data-stu-id="dd213-124">INPUTS</span></span>

### <span data-ttu-id="dd213-125">所有</span><span class="sxs-lookup"><span data-stu-id="dd213-125">None</span></span>

## <span data-ttu-id="dd213-126">輸出</span><span class="sxs-lookup"><span data-stu-id="dd213-126">OUTPUTS</span></span>

### <span data-ttu-id="dd213-127">PSKeyVaultNetworkRuleSet 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dd213-127">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="dd213-128">筆記</span><span class="sxs-lookup"><span data-stu-id="dd213-128">NOTES</span></span>

## <span data-ttu-id="dd213-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd213-129">RELATED LINKS</span></span>
