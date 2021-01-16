---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278508"
---
# <span data-ttu-id="7485f-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="7485f-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="7485f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7485f-102">SYNOPSIS</span></span>
<span data-ttu-id="7485f-103">取得工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7485f-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="7485f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7485f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7485f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7485f-105">DESCRIPTION</span></span>
<span data-ttu-id="7485f-106">**AzOperationalInsightsWorkspaceSharedKey** Cmdlet 會列出工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7485f-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="7485f-107">金鑰是用來將 Operational Insights 代理程式連線至工作區。</span><span class="sxs-lookup"><span data-stu-id="7485f-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="7485f-108">示例</span><span class="sxs-lookup"><span data-stu-id="7485f-108">EXAMPLES</span></span>

### <span data-ttu-id="7485f-109">範例1：依工作區名稱取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="7485f-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="7485f-110">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7485f-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="7485f-111">範例2：使用管線取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="7485f-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="7485f-112">這個命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將工作區傳送到 **AzOperationalInsightsWorkspaceSharedKey** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7485f-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="7485f-113">此命令會取得該工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="7485f-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="7485f-114">參數</span><span class="sxs-lookup"><span data-stu-id="7485f-114">PARAMETERS</span></span>

### <span data-ttu-id="7485f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7485f-115">-DefaultProfile</span></span>
<span data-ttu-id="7485f-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7485f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7485f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="7485f-117">-Name</span></span>
<span data-ttu-id="7485f-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="7485f-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7485f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7485f-119">-ResourceGroupName</span></span>
<span data-ttu-id="7485f-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7485f-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7485f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7485f-121">CommonParameters</span></span>
<span data-ttu-id="7485f-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7485f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7485f-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7485f-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7485f-124">輸入</span><span class="sxs-lookup"><span data-stu-id="7485f-124">INPUTS</span></span>

### <span data-ttu-id="7485f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="7485f-125">System.String</span></span>

## <span data-ttu-id="7485f-126">輸出</span><span class="sxs-lookup"><span data-stu-id="7485f-126">OUTPUTS</span></span>

### <span data-ttu-id="7485f-127">PSWorkspaceKeys 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="7485f-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="7485f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="7485f-128">NOTES</span></span>

## <span data-ttu-id="7485f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="7485f-129">RELATED LINKS</span></span>

[<span data-ttu-id="7485f-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7485f-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="7485f-131">AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7485f-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


