---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100137471"
---
# <span data-ttu-id="0a8df-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="0a8df-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="0a8df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a8df-102">SYNOPSIS</span></span>
<span data-ttu-id="0a8df-103">取得或列出 ACR 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="0a8df-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="0a8df-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a8df-104">SYNTAX</span></span>

### <span data-ttu-id="0a8df-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0a8df-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a8df-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a8df-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a8df-107">說明</span><span class="sxs-lookup"><span data-stu-id="0a8df-107">DESCRIPTION</span></span>
<span data-ttu-id="0a8df-108">取得或列出 ACR 儲存庫。</span><span class="sxs-lookup"><span data-stu-id="0a8df-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="0a8df-109">[清單] 只會傳回儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8df-109">List returns repository names only.</span></span>

## <span data-ttu-id="0a8df-110">示例</span><span class="sxs-lookup"><span data-stu-id="0a8df-110">EXAMPLES</span></span>

### <span data-ttu-id="0a8df-111">範例1</span><span class="sxs-lookup"><span data-stu-id="0a8df-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="0a8df-112">列出註冊表中的所有儲存庫。</span><span class="sxs-lookup"><span data-stu-id="0a8df-112">List all repositories in registry.</span></span>

### <span data-ttu-id="0a8df-113">範例2</span><span class="sxs-lookup"><span data-stu-id="0a8df-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="0a8df-114">在 registry 中列出前3個儲存庫。</span><span class="sxs-lookup"><span data-stu-id="0a8df-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="0a8df-115">範例3</span><span class="sxs-lookup"><span data-stu-id="0a8df-115">Example 3</span></span>
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

<span data-ttu-id="0a8df-116">在註冊表中取得知識庫高山。</span><span class="sxs-lookup"><span data-stu-id="0a8df-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="0a8df-117">參數</span><span class="sxs-lookup"><span data-stu-id="0a8df-117">PARAMETERS</span></span>

### <span data-ttu-id="0a8df-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a8df-118">-DefaultProfile</span></span>
<span data-ttu-id="0a8df-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a8df-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a8df-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a8df-120">-Name</span></span>
<span data-ttu-id="0a8df-121">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="0a8df-121">Repository Name.</span></span>

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

### <span data-ttu-id="0a8df-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0a8df-122">-RegistryName</span></span>
<span data-ttu-id="0a8df-123">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="0a8df-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="0a8df-124">-優先</span><span class="sxs-lookup"><span data-stu-id="0a8df-124">-First</span></span>
<span data-ttu-id="0a8df-125">前 n 個結果。</span><span class="sxs-lookup"><span data-stu-id="0a8df-125">First n results.</span></span>

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

### <span data-ttu-id="0a8df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a8df-126">CommonParameters</span></span>
<span data-ttu-id="0a8df-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a8df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a8df-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a8df-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a8df-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0a8df-129">INPUTS</span></span>

### <span data-ttu-id="0a8df-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0a8df-130">System.String</span></span>

## <span data-ttu-id="0a8df-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0a8df-131">OUTPUTS</span></span>

### <span data-ttu-id="0a8df-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0a8df-132">System.String</span></span>

### <span data-ttu-id="0a8df-133">PSRepositoryAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="0a8df-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="0a8df-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0a8df-134">NOTES</span></span>

## <span data-ttu-id="0a8df-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a8df-135">RELATED LINKS</span></span>
