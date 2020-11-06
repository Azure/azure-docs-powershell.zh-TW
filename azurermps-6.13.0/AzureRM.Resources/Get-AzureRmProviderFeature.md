---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5969a8c5d817f206d45dcbe67d438db3fba955ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448262"
---
# <span data-ttu-id="e2495-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e2495-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="e2495-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2495-102">SYNOPSIS</span></span>
<span data-ttu-id="e2495-103">取得 Azure 提供者功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e2495-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2495-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2495-104">SYNTAX</span></span>

### <span data-ttu-id="e2495-105">ListAvailableParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e2495-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2495-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="e2495-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2495-107">說明</span><span class="sxs-lookup"><span data-stu-id="e2495-107">DESCRIPTION</span></span>
<span data-ttu-id="e2495-108">**AzureRmProviderFeature** Cmdlet 會取得 Azure 提供者功能的功能名稱、提供者名稱及註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="e2495-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="e2495-109">示例</span><span class="sxs-lookup"><span data-stu-id="e2495-109">EXAMPLES</span></span>

### <span data-ttu-id="e2495-110">範例1：取得所有可用的功能</span><span class="sxs-lookup"><span data-stu-id="e2495-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="e2495-111">這個命令會取得所有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="e2495-111">This command gets all available features.</span></span>

### <span data-ttu-id="e2495-112">範例2：取得特定功能的相關資訊</span><span class="sxs-lookup"><span data-stu-id="e2495-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="e2495-113">這個命令會取得指定提供者的功能，其名為 AllowPreReleaseRegions 之功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="e2495-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="e2495-114">參數</span><span class="sxs-lookup"><span data-stu-id="e2495-114">PARAMETERS</span></span>

### <span data-ttu-id="e2495-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2495-115">-DefaultProfile</span></span>
<span data-ttu-id="e2495-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e2495-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2495-117">-功能</span><span class="sxs-lookup"><span data-stu-id="e2495-117">-FeatureName</span></span>
<span data-ttu-id="e2495-118">指定要取得的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="e2495-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="e2495-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="e2495-119">-ListAvailable</span></span>
<span data-ttu-id="e2495-120">表示此 Cmdlet 取得所有功能。</span><span class="sxs-lookup"><span data-stu-id="e2495-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="e2495-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e2495-121">-ProviderNamespace</span></span>
<span data-ttu-id="e2495-122">指定此 Cmdlet 取得提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="e2495-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="e2495-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2495-123">CommonParameters</span></span>
<span data-ttu-id="e2495-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2495-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2495-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2495-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2495-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e2495-126">INPUTS</span></span>

## <span data-ttu-id="e2495-127">輸出</span><span class="sxs-lookup"><span data-stu-id="e2495-127">OUTPUTS</span></span>

## <span data-ttu-id="e2495-128">筆記</span><span class="sxs-lookup"><span data-stu-id="e2495-128">NOTES</span></span>

## <span data-ttu-id="e2495-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2495-129">RELATED LINKS</span></span>

[<span data-ttu-id="e2495-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e2495-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


