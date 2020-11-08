---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryUsage.md
ms.openlocfilehash: 691d8cf006e720d706d2473f76ff8660927e73ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137028"
---
# <span data-ttu-id="c4204-101">Get-AzContainerRegistryUsage</span><span class="sxs-lookup"><span data-stu-id="c4204-101">Get-AzContainerRegistryUsage</span></span>

## <span data-ttu-id="c4204-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4204-102">SYNOPSIS</span></span>
<span data-ttu-id="c4204-103">取得 azure 容器註冊的使用。</span><span class="sxs-lookup"><span data-stu-id="c4204-103">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c4204-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4204-104">SYNTAX</span></span>

```
Get-AzContainerRegistryUsage -ResourceGroupName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4204-105">說明</span><span class="sxs-lookup"><span data-stu-id="c4204-105">DESCRIPTION</span></span>
<span data-ttu-id="c4204-106">取得 azure 容器註冊的使用。</span><span class="sxs-lookup"><span data-stu-id="c4204-106">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c4204-107">示例</span><span class="sxs-lookup"><span data-stu-id="c4204-107">EXAMPLES</span></span>

### <span data-ttu-id="c4204-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c4204-108">Example 1</span></span>
```powershell
PS C:\> Get-AzContainerRegistryUsage -ResourceGroupName $resourceGroupName -RegistryName $RegistryName
```

<span data-ttu-id="c4204-109">取得 azure 容器註冊的使用。</span><span class="sxs-lookup"><span data-stu-id="c4204-109">Get Usage of an azure container registry.</span></span>

## <span data-ttu-id="c4204-110">參數</span><span class="sxs-lookup"><span data-stu-id="c4204-110">PARAMETERS</span></span>

### <span data-ttu-id="c4204-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4204-111">-DefaultProfile</span></span>
<span data-ttu-id="c4204-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4204-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4204-113">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c4204-113">-RegistryName</span></span>
<span data-ttu-id="c4204-114">目標登錄名。</span><span class="sxs-lookup"><span data-stu-id="c4204-114">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4204-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4204-115">-ResourceGroupName</span></span>
<span data-ttu-id="c4204-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c4204-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4204-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4204-117">CommonParameters</span></span>
<span data-ttu-id="c4204-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4204-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4204-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4204-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4204-120">輸入</span><span class="sxs-lookup"><span data-stu-id="c4204-120">INPUTS</span></span>

### <span data-ttu-id="c4204-121">System.object</span><span class="sxs-lookup"><span data-stu-id="c4204-121">System.String</span></span>

## <span data-ttu-id="c4204-122">輸出</span><span class="sxs-lookup"><span data-stu-id="c4204-122">OUTPUTS</span></span>

### <span data-ttu-id="c4204-123">PSRegistryUsage 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="c4204-123">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRegistryUsage</span></span>

## <span data-ttu-id="c4204-124">筆記</span><span class="sxs-lookup"><span data-stu-id="c4204-124">NOTES</span></span>

## <span data-ttu-id="c4204-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4204-125">RELATED LINKS</span></span>
