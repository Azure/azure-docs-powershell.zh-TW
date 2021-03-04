---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915558"
---
# <span data-ttu-id="579f1-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="579f1-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="579f1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="579f1-102">SYNOPSIS</span></span>
<span data-ttu-id="579f1-103">取得或列出 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="579f1-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="579f1-104">語法</span><span class="sxs-lookup"><span data-stu-id="579f1-104">SYNTAX</span></span>

### <span data-ttu-id="579f1-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="579f1-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="579f1-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="579f1-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="579f1-107">描述</span><span class="sxs-lookup"><span data-stu-id="579f1-107">DESCRIPTION</span></span>
<span data-ttu-id="579f1-108">取得或列出 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="579f1-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="579f1-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="579f1-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="579f1-110">第一。</span><span class="sxs-lookup"><span data-stu-id="579f1-110">first.</span></span>

## <span data-ttu-id="579f1-111">例子</span><span class="sxs-lookup"><span data-stu-id="579f1-111">EXAMPLES</span></span>

### <span data-ttu-id="579f1-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="579f1-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="579f1-113">在註冊表之下存放庫高山的清單清單。</span><span class="sxs-lookup"><span data-stu-id="579f1-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="579f1-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="579f1-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="579f1-115">取得清單 sha256：a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="579f1-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="579f1-116">參數</span><span class="sxs-lookup"><span data-stu-id="579f1-116">PARAMETERS</span></span>

### <span data-ttu-id="579f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="579f1-117">-DefaultProfile</span></span>
<span data-ttu-id="579f1-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="579f1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="579f1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="579f1-119">-Name</span></span>
<span data-ttu-id="579f1-120">清單參照。</span><span class="sxs-lookup"><span data-stu-id="579f1-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="579f1-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="579f1-121">-RegistryName</span></span>
<span data-ttu-id="579f1-122">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="579f1-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="579f1-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="579f1-123">-RepositoryName</span></span>
<span data-ttu-id="579f1-124">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="579f1-124">Repository Name.</span></span>

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

### <span data-ttu-id="579f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="579f1-125">CommonParameters</span></span>
<span data-ttu-id="579f1-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="579f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="579f1-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="579f1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="579f1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="579f1-128">INPUTS</span></span>

### <span data-ttu-id="579f1-129">System.String</span><span class="sxs-lookup"><span data-stu-id="579f1-129">System.String</span></span>

## <span data-ttu-id="579f1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="579f1-130">OUTPUTS</span></span>

### <span data-ttu-id="579f1-131">Microsoft.Azure.Commands.ContainerRegistry.models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="579f1-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="579f1-132">Microsoft.Azure.Commands.ContainerRegistry.models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="579f1-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="579f1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="579f1-133">NOTES</span></span>

## <span data-ttu-id="579f1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="579f1-134">RELATED LINKS</span></span>
