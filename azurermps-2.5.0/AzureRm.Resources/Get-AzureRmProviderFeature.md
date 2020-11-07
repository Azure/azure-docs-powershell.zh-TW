---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801162"
---
# <span data-ttu-id="42047-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="42047-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="42047-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42047-102">SYNOPSIS</span></span>
<span data-ttu-id="42047-103">取得 Azure 提供者功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="42047-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42047-104">句法</span><span class="sxs-lookup"><span data-stu-id="42047-104">SYNTAX</span></span>

### <span data-ttu-id="42047-105">ListAvailableParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="42047-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42047-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="42047-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42047-107">說明</span><span class="sxs-lookup"><span data-stu-id="42047-107">DESCRIPTION</span></span>
<span data-ttu-id="42047-108">**AzureRmProviderFeature** Cmdlet 會取得 Azure 提供者功能的功能名稱、提供者名稱及註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="42047-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="42047-109">示例</span><span class="sxs-lookup"><span data-stu-id="42047-109">EXAMPLES</span></span>

### <span data-ttu-id="42047-110">範例1：取得所有可用的功能</span><span class="sxs-lookup"><span data-stu-id="42047-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="42047-111">這個命令會取得所有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="42047-111">This command gets all available features.</span></span>

### <span data-ttu-id="42047-112">範例2：取得特定功能的相關資訊</span><span class="sxs-lookup"><span data-stu-id="42047-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="42047-113">這個命令會取得指定提供者的功能，其名為 AllowPreReleaseRegions 之功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="42047-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="42047-114">參數</span><span class="sxs-lookup"><span data-stu-id="42047-114">PARAMETERS</span></span>

### <span data-ttu-id="42047-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42047-115">-DefaultProfile</span></span>
<span data-ttu-id="42047-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="42047-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42047-117">-功能</span><span class="sxs-lookup"><span data-stu-id="42047-117">-FeatureName</span></span>
<span data-ttu-id="42047-118">指定要取得的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="42047-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="42047-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="42047-119">-ListAvailable</span></span>
<span data-ttu-id="42047-120">表示此 Cmdlet 取得所有功能。</span><span class="sxs-lookup"><span data-stu-id="42047-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="42047-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="42047-121">-ProviderNamespace</span></span>
<span data-ttu-id="42047-122">指定此 Cmdlet 取得提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="42047-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="42047-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42047-123">CommonParameters</span></span>
<span data-ttu-id="42047-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42047-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42047-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42047-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42047-126">輸入</span><span class="sxs-lookup"><span data-stu-id="42047-126">INPUTS</span></span>

## <span data-ttu-id="42047-127">輸出</span><span class="sxs-lookup"><span data-stu-id="42047-127">OUTPUTS</span></span>

## <span data-ttu-id="42047-128">筆記</span><span class="sxs-lookup"><span data-stu-id="42047-128">NOTES</span></span>

## <span data-ttu-id="42047-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="42047-129">RELATED LINKS</span></span>

[<span data-ttu-id="42047-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="42047-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


