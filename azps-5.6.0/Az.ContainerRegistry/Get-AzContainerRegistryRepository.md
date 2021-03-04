---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911737"
---
# <span data-ttu-id="2c6de-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="2c6de-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="2c6de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2c6de-102">SYNOPSIS</span></span>
<span data-ttu-id="2c6de-103">取得或列出 ACR 存放庫。</span><span class="sxs-lookup"><span data-stu-id="2c6de-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="2c6de-104">語法</span><span class="sxs-lookup"><span data-stu-id="2c6de-104">SYNTAX</span></span>

### <span data-ttu-id="2c6de-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2c6de-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c6de-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c6de-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c6de-107">描述</span><span class="sxs-lookup"><span data-stu-id="2c6de-107">DESCRIPTION</span></span>
<span data-ttu-id="2c6de-108">取得或列出 ACR 存放庫。</span><span class="sxs-lookup"><span data-stu-id="2c6de-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="2c6de-109">清單僅會返回存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2c6de-109">List returns repository names only.</span></span>

## <span data-ttu-id="2c6de-110">例子</span><span class="sxs-lookup"><span data-stu-id="2c6de-110">EXAMPLES</span></span>

### <span data-ttu-id="2c6de-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="2c6de-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="2c6de-112">在註冊表中列出所有存放庫。</span><span class="sxs-lookup"><span data-stu-id="2c6de-112">List all repositories in registry.</span></span>

### <span data-ttu-id="2c6de-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="2c6de-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="2c6de-114">在註冊表中列出前 3 個存放庫。</span><span class="sxs-lookup"><span data-stu-id="2c6de-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="2c6de-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="2c6de-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="2c6de-116">在註冊表下取得存放庫高山。</span><span class="sxs-lookup"><span data-stu-id="2c6de-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="2c6de-117">參數</span><span class="sxs-lookup"><span data-stu-id="2c6de-117">PARAMETERS</span></span>

### <span data-ttu-id="2c6de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c6de-118">-DefaultProfile</span></span>
<span data-ttu-id="2c6de-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c6de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c6de-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c6de-120">-Name</span></span>
<span data-ttu-id="2c6de-121">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2c6de-121">Repository Name.</span></span>

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

### <span data-ttu-id="2c6de-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2c6de-122">-RegistryName</span></span>
<span data-ttu-id="2c6de-123">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="2c6de-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="2c6de-124">-第一個</span><span class="sxs-lookup"><span data-stu-id="2c6de-124">-First</span></span>
<span data-ttu-id="2c6de-125">前 n 個結果。</span><span class="sxs-lookup"><span data-stu-id="2c6de-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c6de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c6de-126">CommonParameters</span></span>
<span data-ttu-id="2c6de-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2c6de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c6de-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c6de-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c6de-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2c6de-129">INPUTS</span></span>

### <span data-ttu-id="2c6de-130">System.String</span><span class="sxs-lookup"><span data-stu-id="2c6de-130">System.String</span></span>

## <span data-ttu-id="2c6de-131">輸出</span><span class="sxs-lookup"><span data-stu-id="2c6de-131">OUTPUTS</span></span>

### <span data-ttu-id="2c6de-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2c6de-132">System.String</span></span>

### <span data-ttu-id="2c6de-133">Microsoft.Azure.Commands.ContainerRegistry.models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="2c6de-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="2c6de-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2c6de-134">NOTES</span></span>

## <span data-ttu-id="2c6de-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c6de-135">RELATED LINKS</span></span>
