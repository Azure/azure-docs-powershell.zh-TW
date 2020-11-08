---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 153ed152c68444327f379fda9ab5009290cbc00a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137021"
---
# <span data-ttu-id="ce5d8-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ce5d8-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="ce5d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ce5d8-103">檢查容器註冊名稱的可用性。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="ce5d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce5d8-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ce5d8-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce5d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ce5d8-106">Test-AzContainerRegistryNameAvailability Cmdlet 會檢查容器登錄名稱是否有效且可供使用。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="ce5d8-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce5d8-107">EXAMPLES</span></span>

### <span data-ttu-id="ce5d8-108">範例1：檢查容器註冊名稱的可用性</span><span class="sxs-lookup"><span data-stu-id="ce5d8-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="ce5d8-109">這個命令會檢查容器登錄名稱 SomeRegistryName 的可用性 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="ce5d8-110">參數</span><span class="sxs-lookup"><span data-stu-id="ce5d8-110">PARAMETERS</span></span>

### <span data-ttu-id="ce5d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce5d8-111">-DefaultProfile</span></span>
<span data-ttu-id="ce5d8-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ce5d8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce5d8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce5d8-113">-Name</span></span>
<span data-ttu-id="ce5d8-114">容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="ce5d8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce5d8-115">CommonParameters</span></span>
<span data-ttu-id="ce5d8-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce5d8-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce5d8-118">輸入</span><span class="sxs-lookup"><span data-stu-id="ce5d8-118">INPUTS</span></span>

### <span data-ttu-id="ce5d8-119">System.object</span><span class="sxs-lookup"><span data-stu-id="ce5d8-119">System.String</span></span>

## <span data-ttu-id="ce5d8-120">輸出</span><span class="sxs-lookup"><span data-stu-id="ce5d8-120">OUTPUTS</span></span>

### <span data-ttu-id="ce5d8-121">RegistryNameStatus 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="ce5d8-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="ce5d8-122">筆記</span><span class="sxs-lookup"><span data-stu-id="ce5d8-122">NOTES</span></span>

## <span data-ttu-id="ce5d8-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce5d8-123">RELATED LINKS</span></span>

[<span data-ttu-id="ce5d8-124">新-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ce5d8-124">New-AzContainerRegistry</span></span>]()
