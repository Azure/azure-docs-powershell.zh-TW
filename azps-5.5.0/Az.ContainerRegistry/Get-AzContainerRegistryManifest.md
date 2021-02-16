---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 2fa58235c0ba18042fde13ce9f8d3fb396940d07
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137474"
---
# <span data-ttu-id="96aca-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="96aca-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="96aca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96aca-102">SYNOPSIS</span></span>
<span data-ttu-id="96aca-103">取得或列出 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="96aca-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="96aca-104">句法</span><span class="sxs-lookup"><span data-stu-id="96aca-104">SYNTAX</span></span>

### <span data-ttu-id="96aca-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96aca-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96aca-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="96aca-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96aca-107">說明</span><span class="sxs-lookup"><span data-stu-id="96aca-107">DESCRIPTION</span></span>
<span data-ttu-id="96aca-108">取得或列出 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="96aca-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="96aca-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="96aca-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="96aca-110">一.</span><span class="sxs-lookup"><span data-stu-id="96aca-110">first.</span></span>

## <span data-ttu-id="96aca-111">示例</span><span class="sxs-lookup"><span data-stu-id="96aca-111">EXAMPLES</span></span>

### <span data-ttu-id="96aca-112">範例1</span><span class="sxs-lookup"><span data-stu-id="96aca-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="96aca-113">[註冊表] 底下的 [知識庫高山清單]。</span><span class="sxs-lookup"><span data-stu-id="96aca-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="96aca-114">範例2</span><span class="sxs-lookup"><span data-stu-id="96aca-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="96aca-115">在 registry 中取得資訊清單 sha256： a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 的知識庫高山。</span><span class="sxs-lookup"><span data-stu-id="96aca-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="96aca-116">參數</span><span class="sxs-lookup"><span data-stu-id="96aca-116">PARAMETERS</span></span>

### <span data-ttu-id="96aca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96aca-117">-DefaultProfile</span></span>
<span data-ttu-id="96aca-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96aca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96aca-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="96aca-119">-Name</span></span>
<span data-ttu-id="96aca-120">資訊清單參照。</span><span class="sxs-lookup"><span data-stu-id="96aca-120">Manifest reference.</span></span>

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

### <span data-ttu-id="96aca-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="96aca-121">-RegistryName</span></span>
<span data-ttu-id="96aca-122">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="96aca-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="96aca-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="96aca-123">-RepositoryName</span></span>
<span data-ttu-id="96aca-124">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="96aca-124">Repository Name.</span></span>

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

### <span data-ttu-id="96aca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96aca-125">CommonParameters</span></span>
<span data-ttu-id="96aca-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96aca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96aca-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96aca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96aca-128">輸入</span><span class="sxs-lookup"><span data-stu-id="96aca-128">INPUTS</span></span>

### <span data-ttu-id="96aca-129">System.object</span><span class="sxs-lookup"><span data-stu-id="96aca-129">System.String</span></span>

## <span data-ttu-id="96aca-130">輸出</span><span class="sxs-lookup"><span data-stu-id="96aca-130">OUTPUTS</span></span>

### <span data-ttu-id="96aca-131">PSManifestAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="96aca-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="96aca-132">PSAcrManifest 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="96aca-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="96aca-133">筆記</span><span class="sxs-lookup"><span data-stu-id="96aca-133">NOTES</span></span>

## <span data-ttu-id="96aca-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="96aca-134">RELATED LINKS</span></span>
