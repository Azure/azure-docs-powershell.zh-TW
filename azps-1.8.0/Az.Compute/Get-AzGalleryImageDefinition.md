---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 86da7a6f991bf7eeead14ad3414f9210eb7e175d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93788538"
---
# <span data-ttu-id="fe5e5-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="fe5e5-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="fe5e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe5e5-103">[取得] 或 [清單] 圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="fe5e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe5e5-104">SYNTAX</span></span>

### <span data-ttu-id="fe5e5-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="fe5e5-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe5e5-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="fe5e5-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe5e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="fe5e5-107">DESCRIPTION</span></span>
<span data-ttu-id="fe5e5-108">[取得] 或 [清單] 圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="fe5e5-109">示例</span><span class="sxs-lookup"><span data-stu-id="fe5e5-109">EXAMPLES</span></span>

### <span data-ttu-id="fe5e5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="fe5e5-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="fe5e5-111">取得圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="fe5e5-112">範例2</span><span class="sxs-lookup"><span data-stu-id="fe5e5-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="fe5e5-113">取得以「image」開頭的圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="fe5e5-114">範例3</span><span class="sxs-lookup"><span data-stu-id="fe5e5-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="fe5e5-115">在 gallery1 中取得圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="fe5e5-116">參數</span><span class="sxs-lookup"><span data-stu-id="fe5e5-116">PARAMETERS</span></span>

### <span data-ttu-id="fe5e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe5e5-117">-DefaultProfile</span></span>
<span data-ttu-id="fe5e5-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe5e5-119">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="fe5e5-119">-GalleryName</span></span>
<span data-ttu-id="fe5e5-120">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe5e5-121">-Name</span></span>
<span data-ttu-id="fe5e5-122">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="fe5e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe5e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe5e5-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe5e5-125">-ResourceId</span></span>
<span data-ttu-id="fe5e5-126">畫廊影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fe5e5-126">The resource ID for the gallery image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe5e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe5e5-127">CommonParameters</span></span>
<span data-ttu-id="fe5e5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe5e5-129">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe5e5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="fe5e5-130">INPUTS</span></span>

### <span data-ttu-id="fe5e5-131">System.object</span><span class="sxs-lookup"><span data-stu-id="fe5e5-131">System.String</span></span>

## <span data-ttu-id="fe5e5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fe5e5-132">OUTPUTS</span></span>

### <span data-ttu-id="fe5e5-133">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="fe5e5-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="fe5e5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fe5e5-134">NOTES</span></span>

## <span data-ttu-id="fe5e5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe5e5-135">RELATED LINKS</span></span>
