---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970250"
---
# <span data-ttu-id="f353e-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="f353e-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="f353e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f353e-102">SYNOPSIS</span></span>
<span data-ttu-id="f353e-103">取得工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f353e-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="f353e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f353e-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f353e-105">說明</span><span class="sxs-lookup"><span data-stu-id="f353e-105">DESCRIPTION</span></span>
<span data-ttu-id="f353e-106">**AzOperationalInsightsWorkspace** Cmdlet 會取得現有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f353e-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="f353e-107">如果您指定工作區名稱，此 Cmdlet 會取得該工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f353e-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="f353e-108">如果您沒有指定名稱，此 Cmdlet 會取得資源群組中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f353e-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="f353e-109">如果您沒有指定名稱和資源群組，此 Cmdlet 會取得訂閱中所有工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f353e-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="f353e-110">示例</span><span class="sxs-lookup"><span data-stu-id="f353e-110">EXAMPLES</span></span>

### <span data-ttu-id="f353e-111">範例1：依名稱取得工作區</span><span class="sxs-lookup"><span data-stu-id="f353e-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f353e-112">這個命令會在名為 [ContosoResourceGroup] 的資源群組中取得名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="f353e-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="f353e-113">參數</span><span class="sxs-lookup"><span data-stu-id="f353e-113">PARAMETERS</span></span>

### <span data-ttu-id="f353e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f353e-114">-DefaultProfile</span></span>
<span data-ttu-id="f353e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f353e-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f353e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f353e-116">-Name</span></span>
<span data-ttu-id="f353e-117">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f353e-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f353e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f353e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f353e-119">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f353e-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f353e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f353e-120">CommonParameters</span></span>
<span data-ttu-id="f353e-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f353e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f353e-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f353e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f353e-123">輸入</span><span class="sxs-lookup"><span data-stu-id="f353e-123">INPUTS</span></span>

### <span data-ttu-id="f353e-124">System.object</span><span class="sxs-lookup"><span data-stu-id="f353e-124">System.String</span></span>

## <span data-ttu-id="f353e-125">輸出</span><span class="sxs-lookup"><span data-stu-id="f353e-125">OUTPUTS</span></span>

### <span data-ttu-id="f353e-126">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="f353e-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="f353e-127">筆記</span><span class="sxs-lookup"><span data-stu-id="f353e-127">NOTES</span></span>

## <span data-ttu-id="f353e-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="f353e-128">RELATED LINKS</span></span>

[<span data-ttu-id="f353e-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f353e-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


