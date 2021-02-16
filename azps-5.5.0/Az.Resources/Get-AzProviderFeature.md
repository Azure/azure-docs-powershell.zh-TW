---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132255"
---
# <span data-ttu-id="fccae-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fccae-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="fccae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fccae-102">SYNOPSIS</span></span>
<span data-ttu-id="fccae-103">取得 Azure 提供者功能的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fccae-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="fccae-104">句法</span><span class="sxs-lookup"><span data-stu-id="fccae-104">SYNTAX</span></span>

### <span data-ttu-id="fccae-105">ListAvailableParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fccae-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fccae-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="fccae-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fccae-107">說明</span><span class="sxs-lookup"><span data-stu-id="fccae-107">DESCRIPTION</span></span>
<span data-ttu-id="fccae-108">**AzProviderFeature** Cmdlet 會取得 Azure 提供者功能的功能名稱、提供者名稱及註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="fccae-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="fccae-109">示例</span><span class="sxs-lookup"><span data-stu-id="fccae-109">EXAMPLES</span></span>

### <span data-ttu-id="fccae-110">範例1：取得所有可用的功能</span><span class="sxs-lookup"><span data-stu-id="fccae-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="fccae-111">這個命令會取得所有可用的功能。</span><span class="sxs-lookup"><span data-stu-id="fccae-111">This command gets all available features.</span></span>

### <span data-ttu-id="fccae-112">範例2：取得特定功能的相關資訊</span><span class="sxs-lookup"><span data-stu-id="fccae-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="fccae-113">這個命令會取得指定提供者的功能，其名為 AllowPreReleaseRegions 之功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="fccae-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="fccae-114">參數</span><span class="sxs-lookup"><span data-stu-id="fccae-114">PARAMETERS</span></span>

### <span data-ttu-id="fccae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fccae-115">-DefaultProfile</span></span>
<span data-ttu-id="fccae-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fccae-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fccae-117">-功能</span><span class="sxs-lookup"><span data-stu-id="fccae-117">-FeatureName</span></span>
<span data-ttu-id="fccae-118">指定要取得的功能名稱。</span><span class="sxs-lookup"><span data-stu-id="fccae-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="fccae-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="fccae-119">-ListAvailable</span></span>
<span data-ttu-id="fccae-120">表示此 Cmdlet 取得所有功能。</span><span class="sxs-lookup"><span data-stu-id="fccae-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="fccae-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fccae-121">-ProviderNamespace</span></span>
<span data-ttu-id="fccae-122">指定此 Cmdlet 取得提供者功能的命名空間。</span><span class="sxs-lookup"><span data-stu-id="fccae-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="fccae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fccae-123">CommonParameters</span></span>
<span data-ttu-id="fccae-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fccae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fccae-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fccae-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fccae-126">輸入</span><span class="sxs-lookup"><span data-stu-id="fccae-126">INPUTS</span></span>

### <span data-ttu-id="fccae-127">System.object</span><span class="sxs-lookup"><span data-stu-id="fccae-127">System.String</span></span>

## <span data-ttu-id="fccae-128">輸出</span><span class="sxs-lookup"><span data-stu-id="fccae-128">OUTPUTS</span></span>

### <span data-ttu-id="fccae-129">PSProviderFeature 中的 SdkModels （）</span><span class="sxs-lookup"><span data-stu-id="fccae-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="fccae-130">筆記</span><span class="sxs-lookup"><span data-stu-id="fccae-130">NOTES</span></span>

## <span data-ttu-id="fccae-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="fccae-131">RELATED LINKS</span></span>

[<span data-ttu-id="fccae-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fccae-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)


