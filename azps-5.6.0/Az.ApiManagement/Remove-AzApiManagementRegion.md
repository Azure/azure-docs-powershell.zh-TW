---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916682"
---
# <span data-ttu-id="64055-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="64055-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="64055-102">簡介</span><span class="sxs-lookup"><span data-stu-id="64055-102">SYNOPSIS</span></span>
<span data-ttu-id="64055-103">從 PsApiManagement 實例移除現有的部署區域。</span><span class="sxs-lookup"><span data-stu-id="64055-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="64055-104">語法</span><span class="sxs-lookup"><span data-stu-id="64055-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64055-105">描述</span><span class="sxs-lookup"><span data-stu-id="64055-105">DESCRIPTION</span></span>
<span data-ttu-id="64055-106">**Remove-AzApiManagementRegion** Cmdlet 會從提供的 **Microsoft.Azure.Commands.ApiManagement.models.PsApiManagementRegion 類型實例集合移除 Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement.**  </span><span class="sxs-lookup"><span data-stu-id="64055-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="64055-107">此 Cmdlet 不會自行修改部署，但會更新 **記憶體中的 PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="64055-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="64055-108">若要更新 API 管理部署，請傳遞已修改的 **PsApiManagementInstance** 到 **Set-AzApiManagement。**</span><span class="sxs-lookup"><span data-stu-id="64055-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="64055-109">例子</span><span class="sxs-lookup"><span data-stu-id="64055-109">EXAMPLES</span></span>

### <span data-ttu-id="64055-110">範例 1：從 PsApiManagement 實例移除區域</span><span class="sxs-lookup"><span data-stu-id="64055-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="64055-111">此命令會從 **PsApiManagement** 實例移除名為 East US 的區域。</span><span class="sxs-lookup"><span data-stu-id="64055-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="64055-112">範例 2：使用一系列命令從 PsApiManagement 實例移除區域</span><span class="sxs-lookup"><span data-stu-id="64055-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="64055-113">第一個命令會從名為 ContosoApi 的資源群組中，獲得 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="64055-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="64055-114">最後一個命令接著會從該實例移除名為 East US 的區域，然後更新部署。</span><span class="sxs-lookup"><span data-stu-id="64055-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="64055-115">參數</span><span class="sxs-lookup"><span data-stu-id="64055-115">PARAMETERS</span></span>

### <span data-ttu-id="64055-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="64055-116">-ApiManagement</span></span>
<span data-ttu-id="64055-117">指定此 Cmdlet 移除其他部署地區的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="64055-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64055-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64055-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="64055-119">-位置</span><span class="sxs-lookup"><span data-stu-id="64055-119">-Location</span></span>
<span data-ttu-id="64055-120">指定此 Cmdlet 移除的區域位置。</span><span class="sxs-lookup"><span data-stu-id="64055-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="64055-121">指定 Api 管理服務支援區域之間的新部署區域位置。</span><span class="sxs-lookup"><span data-stu-id="64055-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="64055-122">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" |其中 {$_.ResourceTypes[0]。ResourceTypeName -eq "service"} |Select-Object位置</span><span class="sxs-lookup"><span data-stu-id="64055-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64055-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64055-123">CommonParameters</span></span>
<span data-ttu-id="64055-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="64055-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64055-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64055-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64055-126">輸入</span><span class="sxs-lookup"><span data-stu-id="64055-126">INPUTS</span></span>

### <span data-ttu-id="64055-127">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="64055-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="64055-128">System.String</span><span class="sxs-lookup"><span data-stu-id="64055-128">System.String</span></span>

## <span data-ttu-id="64055-129">輸出</span><span class="sxs-lookup"><span data-stu-id="64055-129">OUTPUTS</span></span>

### <span data-ttu-id="64055-130">Microsoft.Azure.Commands.ApiManagement.models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="64055-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="64055-131">筆記</span><span class="sxs-lookup"><span data-stu-id="64055-131">NOTES</span></span>

## <span data-ttu-id="64055-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="64055-132">RELATED LINKS</span></span>

[<span data-ttu-id="64055-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="64055-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="64055-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="64055-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


