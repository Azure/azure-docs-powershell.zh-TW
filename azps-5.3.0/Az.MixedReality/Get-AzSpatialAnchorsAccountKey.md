---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437980"
---
# <span data-ttu-id="d010b-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="d010b-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="d010b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d010b-102">SYNOPSIS</span></span>
<span data-ttu-id="d010b-103">取得空間錨定帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="d010b-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="d010b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d010b-104">SYNTAX</span></span>

### <span data-ttu-id="d010b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d010b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d010b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d010b-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d010b-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="d010b-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d010b-108">說明</span><span class="sxs-lookup"><span data-stu-id="d010b-108">DESCRIPTION</span></span>
<span data-ttu-id="d010b-109">取得 [空間錨點] 帳戶的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="d010b-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="d010b-110">示例</span><span class="sxs-lookup"><span data-stu-id="d010b-110">EXAMPLES</span></span>

### <span data-ttu-id="d010b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d010b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="d010b-112">從目前的訂閱和資源群組 "rg1"，取得空間定位帳戶「範例」的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="d010b-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="d010b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="d010b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="d010b-114">從目前的訂閱和含有管道的資源群組 "rg1" 取得空間錨點 "範例" 的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="d010b-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="d010b-115">參數</span><span class="sxs-lookup"><span data-stu-id="d010b-115">PARAMETERS</span></span>

### <span data-ttu-id="d010b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d010b-116">-DefaultProfile</span></span>
<span data-ttu-id="d010b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d010b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d010b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d010b-118">-InputObject</span></span>
<span data-ttu-id="d010b-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="d010b-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d010b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d010b-120">-Name</span></span>
<span data-ttu-id="d010b-121">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d010b-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d010b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d010b-122">-ResourceGroupName</span></span>
<span data-ttu-id="d010b-123">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d010b-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d010b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d010b-124">-ResourceId</span></span>
<span data-ttu-id="d010b-125">空間錨定帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d010b-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="d010b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d010b-126">CommonParameters</span></span>
<span data-ttu-id="d010b-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d010b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d010b-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d010b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d010b-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d010b-129">INPUTS</span></span>

### <span data-ttu-id="d010b-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d010b-130">System.String</span></span>

### <span data-ttu-id="d010b-131">MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d010b-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d010b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="d010b-132">OUTPUTS</span></span>

### <span data-ttu-id="d010b-133">MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d010b-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="d010b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="d010b-134">NOTES</span></span>

## <span data-ttu-id="d010b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="d010b-135">RELATED LINKS</span></span>
