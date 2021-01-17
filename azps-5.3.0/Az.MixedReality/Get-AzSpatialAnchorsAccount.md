---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437983"
---
# <span data-ttu-id="d5981-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d5981-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d5981-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d5981-102">SYNOPSIS</span></span>
<span data-ttu-id="d5981-103">取得空間錨定帳戶</span><span class="sxs-lookup"><span data-stu-id="d5981-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="d5981-104">句法</span><span class="sxs-lookup"><span data-stu-id="d5981-104">SYNTAX</span></span>

### <span data-ttu-id="d5981-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d5981-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5981-106">GetParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d5981-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5981-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5981-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5981-108">說明</span><span class="sxs-lookup"><span data-stu-id="d5981-108">DESCRIPTION</span></span>
<span data-ttu-id="d5981-109">在特定訂閱和資源群組中取得或列出空間錨點帳戶 (s) 。</span><span class="sxs-lookup"><span data-stu-id="d5981-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="d5981-110">示例</span><span class="sxs-lookup"><span data-stu-id="d5981-110">EXAMPLES</span></span>

### <span data-ttu-id="d5981-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d5981-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="d5981-112">列出 [資源] 群組中的所有空間錨點帳戶 [rg1]。</span><span class="sxs-lookup"><span data-stu-id="d5981-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="d5981-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d5981-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="d5981-114">取得資源群組 "rg1" 中的空間錨記帳戶「範例」。</span><span class="sxs-lookup"><span data-stu-id="d5981-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="d5981-115">參數</span><span class="sxs-lookup"><span data-stu-id="d5981-115">PARAMETERS</span></span>

### <span data-ttu-id="d5981-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5981-116">-DefaultProfile</span></span>
<span data-ttu-id="d5981-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d5981-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5981-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="d5981-118">-Name</span></span>
<span data-ttu-id="d5981-119">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d5981-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5981-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5981-120">-ResourceGroupName</span></span>
<span data-ttu-id="d5981-121">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d5981-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5981-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5981-122">-ResourceId</span></span>
<span data-ttu-id="d5981-123">空間錨定帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d5981-123">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5981-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5981-124">CommonParameters</span></span>
<span data-ttu-id="d5981-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d5981-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d5981-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d5981-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5981-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d5981-127">INPUTS</span></span>

### <span data-ttu-id="d5981-128">System.object</span><span class="sxs-lookup"><span data-stu-id="d5981-128">System.String</span></span>

## <span data-ttu-id="d5981-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d5981-129">OUTPUTS</span></span>

### <span data-ttu-id="d5981-130">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d5981-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d5981-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d5981-131">NOTES</span></span>

## <span data-ttu-id="d5981-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d5981-132">RELATED LINKS</span></span>
