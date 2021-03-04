---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseWorkspace.md
ms.openlocfilehash: e92b4d20e89df451c483bc0b4bdccb83fdc8a140
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916826"
---
# <span data-ttu-id="76030-101">Test-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="76030-101">Test-AzSynapseWorkspace</span></span>

## <span data-ttu-id="76030-102">簡介</span><span class="sxs-lookup"><span data-stu-id="76030-102">SYNOPSIS</span></span>
<span data-ttu-id="76030-103">檢查 Synapse Analytics 工作區是否存在。</span><span class="sxs-lookup"><span data-stu-id="76030-103">Checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="76030-104">語法</span><span class="sxs-lookup"><span data-stu-id="76030-104">SYNTAX</span></span>

```
Test-AzSynapseWorkspace [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76030-105">描述</span><span class="sxs-lookup"><span data-stu-id="76030-105">DESCRIPTION</span></span>
<span data-ttu-id="76030-106">**Test-AzSynapseWorkspace** Cmdlet 會檢查 Synapse Analytics 工作區是否存在。</span><span class="sxs-lookup"><span data-stu-id="76030-106">The **Test-AzSynapseWorkspace** cmdlet checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="76030-107">例子</span><span class="sxs-lookup"><span data-stu-id="76030-107">EXAMPLES</span></span>

### <span data-ttu-id="76030-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="76030-108">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="76030-109">此命令會檢查 Synapse Analytics 工作區是否存在。</span><span class="sxs-lookup"><span data-stu-id="76030-109">This command checks for the existence of a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="76030-110">參數</span><span class="sxs-lookup"><span data-stu-id="76030-110">PARAMETERS</span></span>

### <span data-ttu-id="76030-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76030-111">-DefaultProfile</span></span>
<span data-ttu-id="76030-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="76030-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76030-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="76030-113">-Name</span></span>
<span data-ttu-id="76030-114">Synapse 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="76030-114">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76030-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76030-115">-ResourceGroupName</span></span>
<span data-ttu-id="76030-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="76030-116">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76030-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76030-117">CommonParameters</span></span>
<span data-ttu-id="76030-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="76030-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76030-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76030-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76030-120">輸入</span><span class="sxs-lookup"><span data-stu-id="76030-120">INPUTS</span></span>

### <span data-ttu-id="76030-121">沒有</span><span class="sxs-lookup"><span data-stu-id="76030-121">None</span></span>

## <span data-ttu-id="76030-122">輸出</span><span class="sxs-lookup"><span data-stu-id="76030-122">OUTPUTS</span></span>

### <span data-ttu-id="76030-123">System.Object</span><span class="sxs-lookup"><span data-stu-id="76030-123">System.Object</span></span>
## <span data-ttu-id="76030-124">筆記</span><span class="sxs-lookup"><span data-stu-id="76030-124">NOTES</span></span>

## <span data-ttu-id="76030-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="76030-125">RELATED LINKS</span></span>
