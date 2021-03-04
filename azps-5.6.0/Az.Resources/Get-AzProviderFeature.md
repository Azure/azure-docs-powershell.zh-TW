---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: 67a0eee0dfe46b7b846958e1aa3f2be515a6b213
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917934"
---
# <span data-ttu-id="3d3ff-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3d3ff-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="3d3ff-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3d3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3ff-103">瞭解 Azure 提供者功能。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="3d3ff-104">語法</span><span class="sxs-lookup"><span data-stu-id="3d3ff-104">SYNTAX</span></span>

### <span data-ttu-id="3d3ff-105">ListAvailableParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3d3ff-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3d3ff-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="3d3ff-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d3ff-107">描述</span><span class="sxs-lookup"><span data-stu-id="3d3ff-107">DESCRIPTION</span></span>
<span data-ttu-id="3d3ff-108">**Get-AzProviderFeature** Cmdlet 會取得 Azure 提供者功能的功能名稱、提供者名稱和註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="3d3ff-109">例子</span><span class="sxs-lookup"><span data-stu-id="3d3ff-109">EXAMPLES</span></span>

### <span data-ttu-id="3d3ff-110">範例 1：取得所有可用的功能</span><span class="sxs-lookup"><span data-stu-id="3d3ff-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="3d3ff-111">此命令會獲得所有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-111">This command gets all available features.</span></span>

### <span data-ttu-id="3d3ff-112">範例 2：取得特定功能的資訊</span><span class="sxs-lookup"><span data-stu-id="3d3ff-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="3d3ff-113">此命令會針對指定提供者的 AllowPreReleaseRegions 功能，獲得相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="3d3ff-114">參數</span><span class="sxs-lookup"><span data-stu-id="3d3ff-114">PARAMETERS</span></span>

### <span data-ttu-id="3d3ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3ff-115">-DefaultProfile</span></span>
<span data-ttu-id="3d3ff-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3d3ff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d3ff-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="3d3ff-117">-FeatureName</span></span>
<span data-ttu-id="3d3ff-118">指定要取得的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ff-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="3d3ff-119">-ListAvailable</span></span>
<span data-ttu-id="3d3ff-120">表示此 Cmdlet 會獲得所有功能。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ff-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="3d3ff-121">-ProviderNamespace</span></span>
<span data-ttu-id="3d3ff-122">指定此 Cmdlet 可獲取提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3ff-123">CommonParameters</span></span>
<span data-ttu-id="3d3ff-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3d3ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3ff-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d3ff-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3ff-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3d3ff-126">INPUTS</span></span>

### <span data-ttu-id="3d3ff-127">System.String</span><span class="sxs-lookup"><span data-stu-id="3d3ff-127">System.String</span></span>

## <span data-ttu-id="3d3ff-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3d3ff-128">OUTPUTS</span></span>

### <span data-ttu-id="3d3ff-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3d3ff-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="3d3ff-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3d3ff-130">NOTES</span></span>

## <span data-ttu-id="3d3ff-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d3ff-131">RELATED LINKS</span></span>

[<span data-ttu-id="3d3ff-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="3d3ff-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


