---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911726"
---
# <span data-ttu-id="3586b-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="3586b-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="3586b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3586b-102">SYNOPSIS</span></span>
<span data-ttu-id="3586b-103">取得或列出 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="3586b-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="3586b-104">語法</span><span class="sxs-lookup"><span data-stu-id="3586b-104">SYNTAX</span></span>

### <span data-ttu-id="3586b-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3586b-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3586b-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="3586b-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3586b-107">描述</span><span class="sxs-lookup"><span data-stu-id="3586b-107">DESCRIPTION</span></span>
<span data-ttu-id="3586b-108">取得或列出 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="3586b-108">Get or list ACR tag.</span></span>
<span data-ttu-id="3586b-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="3586b-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="3586b-110">第一。</span><span class="sxs-lookup"><span data-stu-id="3586b-110">first.</span></span>

## <span data-ttu-id="3586b-111">例子</span><span class="sxs-lookup"><span data-stu-id="3586b-111">EXAMPLES</span></span>

### <span data-ttu-id="3586b-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="3586b-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="3586b-113">在註冊表下列出存放庫高山的標記。</span><span class="sxs-lookup"><span data-stu-id="3586b-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="3586b-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="3586b-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="3586b-115">在註冊表下取得存放庫高山的最新標記。</span><span class="sxs-lookup"><span data-stu-id="3586b-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="3586b-116">參數</span><span class="sxs-lookup"><span data-stu-id="3586b-116">PARAMETERS</span></span>

### <span data-ttu-id="3586b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3586b-117">-DefaultProfile</span></span>
<span data-ttu-id="3586b-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3586b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3586b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3586b-119">-Name</span></span>
<span data-ttu-id="3586b-120">標記。</span><span class="sxs-lookup"><span data-stu-id="3586b-120">Tag.</span></span>

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

### <span data-ttu-id="3586b-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="3586b-121">-RegistryName</span></span>
<span data-ttu-id="3586b-122">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="3586b-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="3586b-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="3586b-123">-RepositoryName</span></span>
<span data-ttu-id="3586b-124">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="3586b-124">Repository Name.</span></span>

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

### <span data-ttu-id="3586b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3586b-125">CommonParameters</span></span>
<span data-ttu-id="3586b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3586b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3586b-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3586b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3586b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3586b-128">INPUTS</span></span>

### <span data-ttu-id="3586b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="3586b-129">System.String</span></span>

## <span data-ttu-id="3586b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3586b-130">OUTPUTS</span></span>

### <span data-ttu-id="3586b-131">Microsoft.Azure.Commands.ContainerRegistry.models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="3586b-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="3586b-132">Microsoft.Azure.Commands.ContainerRegistry.models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="3586b-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="3586b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3586b-133">NOTES</span></span>

## <span data-ttu-id="3586b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3586b-134">RELATED LINKS</span></span>
