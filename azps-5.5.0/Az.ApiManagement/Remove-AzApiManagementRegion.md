---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100143523"
---
# <span data-ttu-id="0c195-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0c195-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="0c195-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c195-102">SYNOPSIS</span></span>
<span data-ttu-id="0c195-103">從 PsApiManagement 實例移除現有的部署區域。</span><span class="sxs-lookup"><span data-stu-id="0c195-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="0c195-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c195-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c195-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c195-105">DESCRIPTION</span></span>
<span data-ttu-id="0c195-106">AzApiManagementRegion Cmdlet 會從已提供 type **PsApiManagementRegion ApiManagement** 的實例的 AdditionalRegions 集合中移除類型的實例，**並** 從 **的** 中移除的 **。**</span><span class="sxs-lookup"><span data-stu-id="0c195-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0c195-107">這個 Cmdlet 不會自行修改部署，但會更新記憶體中 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="0c195-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0c195-108">若要更新 API 管理的部署，請將修改過的 **PsApiManagementInstance** 傳遞到 **AzApiManagement**。</span><span class="sxs-lookup"><span data-stu-id="0c195-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="0c195-109">示例</span><span class="sxs-lookup"><span data-stu-id="0c195-109">EXAMPLES</span></span>

### <span data-ttu-id="0c195-110">範例1：從 PsApiManagement 實例中移除區域</span><span class="sxs-lookup"><span data-stu-id="0c195-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="0c195-111">這個命令會從 **PsApiManagement** 實例中移除名為「美國東部」的地區。</span><span class="sxs-lookup"><span data-stu-id="0c195-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="0c195-112">範例2：使用一系列命令從 PsApiManagement 實例中移除區域</span><span class="sxs-lookup"><span data-stu-id="0c195-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="0c195-113">這個第一個命令會從名為 Contoso 的資源群組（名為 ContosoApi）中取得 **PsApiManagement** 的實例。</span><span class="sxs-lookup"><span data-stu-id="0c195-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="0c195-114">然後，最後一個命令會從該實例移除名為 East 的地區，然後更新部署。</span><span class="sxs-lookup"><span data-stu-id="0c195-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="0c195-115">參數</span><span class="sxs-lookup"><span data-stu-id="0c195-115">PARAMETERS</span></span>

### <span data-ttu-id="0c195-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0c195-116">-ApiManagement</span></span>
<span data-ttu-id="0c195-117">指定此 Cmdlet 移除其他部署區域的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="0c195-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="0c195-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c195-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="0c195-119">-位置</span><span class="sxs-lookup"><span data-stu-id="0c195-119">-Location</span></span>
<span data-ttu-id="0c195-120">指定此 Cmdlet 移除之區域的位置。</span><span class="sxs-lookup"><span data-stu-id="0c195-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="0c195-121">指定新部署區域在 Api 管理服務支援區域之間的位置。</span><span class="sxs-lookup"><span data-stu-id="0c195-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="0c195-122">若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置</span><span class="sxs-lookup"><span data-stu-id="0c195-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="0c195-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c195-123">CommonParameters</span></span>
<span data-ttu-id="0c195-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c195-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c195-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0c195-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c195-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0c195-126">INPUTS</span></span>

### <span data-ttu-id="0c195-127">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="0c195-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="0c195-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0c195-128">System.String</span></span>

## <span data-ttu-id="0c195-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0c195-129">OUTPUTS</span></span>

### <span data-ttu-id="0c195-130">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="0c195-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0c195-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0c195-131">NOTES</span></span>

## <span data-ttu-id="0c195-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c195-132">RELATED LINKS</span></span>

[<span data-ttu-id="0c195-133">附加 AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0c195-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="0c195-134">更新-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0c195-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


