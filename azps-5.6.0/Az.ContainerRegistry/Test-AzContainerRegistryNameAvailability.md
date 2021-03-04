---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903006"
---
# <span data-ttu-id="37211-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="37211-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="37211-102">簡介</span><span class="sxs-lookup"><span data-stu-id="37211-102">SYNOPSIS</span></span>
<span data-ttu-id="37211-103">檢查容器註冊表名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="37211-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="37211-104">語法</span><span class="sxs-lookup"><span data-stu-id="37211-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37211-105">描述</span><span class="sxs-lookup"><span data-stu-id="37211-105">DESCRIPTION</span></span>
<span data-ttu-id="37211-106">此Test-AzContainerRegistryNameAvailability Cmdlet 會檢查容器註冊表名稱是否有效且可以使用。</span><span class="sxs-lookup"><span data-stu-id="37211-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="37211-107">例子</span><span class="sxs-lookup"><span data-stu-id="37211-107">EXAMPLES</span></span>

### <span data-ttu-id="37211-108">範例 1：檢查容器註冊表名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="37211-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="37211-109">此命令會檢查容器註冊表名稱 \` SomeRegistryName 的可用性 \` 。</span><span class="sxs-lookup"><span data-stu-id="37211-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="37211-110">參數</span><span class="sxs-lookup"><span data-stu-id="37211-110">PARAMETERS</span></span>

### <span data-ttu-id="37211-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37211-111">-DefaultProfile</span></span>
<span data-ttu-id="37211-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="37211-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37211-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="37211-113">-Name</span></span>
<span data-ttu-id="37211-114">容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="37211-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37211-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37211-115">CommonParameters</span></span>
<span data-ttu-id="37211-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="37211-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37211-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37211-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37211-118">輸入</span><span class="sxs-lookup"><span data-stu-id="37211-118">INPUTS</span></span>

### <span data-ttu-id="37211-119">System.String</span><span class="sxs-lookup"><span data-stu-id="37211-119">System.String</span></span>

## <span data-ttu-id="37211-120">輸出</span><span class="sxs-lookup"><span data-stu-id="37211-120">OUTPUTS</span></span>

### <span data-ttu-id="37211-121">Microsoft.Azure.management.ContainerRegistry.models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="37211-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="37211-122">筆記</span><span class="sxs-lookup"><span data-stu-id="37211-122">NOTES</span></span>

## <span data-ttu-id="37211-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="37211-123">RELATED LINKS</span></span>

[<span data-ttu-id="37211-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="37211-124">New-AzContainerRegistry</span></span>]()

