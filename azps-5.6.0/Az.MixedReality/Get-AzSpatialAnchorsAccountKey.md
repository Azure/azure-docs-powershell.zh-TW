---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 351b7a2412a861fcebc456d165e9fc4eddea5122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903189"
---
# <span data-ttu-id="a4075-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="a4075-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="a4075-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a4075-102">SYNOPSIS</span></span>
<span data-ttu-id="a4075-103">取得空間錨點帳戶的金鑰</span><span class="sxs-lookup"><span data-stu-id="a4075-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="a4075-104">語法</span><span class="sxs-lookup"><span data-stu-id="a4075-104">SYNTAX</span></span>

### <span data-ttu-id="a4075-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a4075-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4075-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4075-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4075-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4075-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4075-108">描述</span><span class="sxs-lookup"><span data-stu-id="a4075-108">DESCRIPTION</span></span>
<span data-ttu-id="a4075-109">取得空間錨點帳戶的開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4075-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="a4075-110">例子</span><span class="sxs-lookup"><span data-stu-id="a4075-110">EXAMPLES</span></span>

### <span data-ttu-id="a4075-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a4075-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a4075-112">從目前的訂閱和資源群組 "rg1" 取得空間錨點帳戶的開發人員金鑰「範例」。</span><span class="sxs-lookup"><span data-stu-id="a4075-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="a4075-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a4075-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="a4075-114">從目前的訂閱和資源群組 "rg1" 取得具有管道的「空間錨點帳戶」「範例」開發人員金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4075-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="a4075-115">參數</span><span class="sxs-lookup"><span data-stu-id="a4075-115">PARAMETERS</span></span>

### <span data-ttu-id="a4075-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4075-116">-DefaultProfile</span></span>
<span data-ttu-id="a4075-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a4075-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4075-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4075-118">-InputObject</span></span>
<span data-ttu-id="a4075-119">自訂網域物件。</span><span class="sxs-lookup"><span data-stu-id="a4075-119">The custom domain object.</span></span>

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

### <span data-ttu-id="a4075-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="a4075-120">-Name</span></span>
<span data-ttu-id="a4075-121">空間錨點帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a4075-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="a4075-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4075-122">-ResourceGroupName</span></span>
<span data-ttu-id="a4075-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a4075-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="a4075-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4075-124">-ResourceId</span></span>
<span data-ttu-id="a4075-125">空間錨點帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a4075-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="a4075-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4075-126">CommonParameters</span></span>
<span data-ttu-id="a4075-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a4075-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a4075-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a4075-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4075-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a4075-129">INPUTS</span></span>

### <span data-ttu-id="a4075-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a4075-130">System.String</span></span>

### <span data-ttu-id="a4075-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a4075-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a4075-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a4075-132">OUTPUTS</span></span>

### <span data-ttu-id="a4075-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a4075-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="a4075-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a4075-134">NOTES</span></span>

## <span data-ttu-id="a4075-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a4075-135">RELATED LINKS</span></span>
