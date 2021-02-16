---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 88bf3648f416efa69576c6b09a0d59f0d0d0fa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129754"
---
# <span data-ttu-id="2741b-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="2741b-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="2741b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2741b-102">SYNOPSIS</span></span>
<span data-ttu-id="2741b-103">取得或列出 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="2741b-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="2741b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2741b-104">SYNTAX</span></span>

### <span data-ttu-id="2741b-105">ListParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2741b-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2741b-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="2741b-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2741b-107">說明</span><span class="sxs-lookup"><span data-stu-id="2741b-107">DESCRIPTION</span></span>
<span data-ttu-id="2741b-108">取得或列出 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="2741b-108">Get or list ACR tag.</span></span>
<span data-ttu-id="2741b-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="2741b-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="2741b-110">一.</span><span class="sxs-lookup"><span data-stu-id="2741b-110">first.</span></span>

## <span data-ttu-id="2741b-111">示例</span><span class="sxs-lookup"><span data-stu-id="2741b-111">EXAMPLES</span></span>

### <span data-ttu-id="2741b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="2741b-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="2741b-113">[註冊表] 底下 [知識庫高山] 的清單標記。</span><span class="sxs-lookup"><span data-stu-id="2741b-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="2741b-114">範例2</span><span class="sxs-lookup"><span data-stu-id="2741b-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="2741b-115">在 [登錄] 底下取得 [知識庫高山的最新標誌]。</span><span class="sxs-lookup"><span data-stu-id="2741b-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="2741b-116">參數</span><span class="sxs-lookup"><span data-stu-id="2741b-116">PARAMETERS</span></span>

### <span data-ttu-id="2741b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2741b-117">-DefaultProfile</span></span>
<span data-ttu-id="2741b-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2741b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2741b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2741b-119">-Name</span></span>
<span data-ttu-id="2741b-120">標記.</span><span class="sxs-lookup"><span data-stu-id="2741b-120">Tag.</span></span>

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

### <span data-ttu-id="2741b-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2741b-121">-RegistryName</span></span>
<span data-ttu-id="2741b-122">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="2741b-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="2741b-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="2741b-123">-RepositoryName</span></span>
<span data-ttu-id="2741b-124">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="2741b-124">Repository Name.</span></span>

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

### <span data-ttu-id="2741b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2741b-125">CommonParameters</span></span>
<span data-ttu-id="2741b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2741b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2741b-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2741b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2741b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="2741b-128">INPUTS</span></span>

### <span data-ttu-id="2741b-129">System.object</span><span class="sxs-lookup"><span data-stu-id="2741b-129">System.String</span></span>

## <span data-ttu-id="2741b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2741b-130">OUTPUTS</span></span>

### <span data-ttu-id="2741b-131">PSTagAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="2741b-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="2741b-132">PSTagList 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="2741b-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="2741b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="2741b-133">NOTES</span></span>

## <span data-ttu-id="2741b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="2741b-134">RELATED LINKS</span></span>
