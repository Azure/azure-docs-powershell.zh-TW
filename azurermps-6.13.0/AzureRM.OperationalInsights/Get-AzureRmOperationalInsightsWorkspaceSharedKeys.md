---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 07d0834b89010ff533e1620f29904ea159d3dfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625575"
---
# <span data-ttu-id="b0a51-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="b0a51-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="b0a51-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b0a51-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a51-103">取得工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b0a51-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0a51-104">句法</span><span class="sxs-lookup"><span data-stu-id="b0a51-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0a51-105">說明</span><span class="sxs-lookup"><span data-stu-id="b0a51-105">DESCRIPTION</span></span>
<span data-ttu-id="b0a51-106">**AzureRmOperationalInsightsWorkspaceSharedKeys** Cmdlet 會列出工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b0a51-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="b0a51-107">金鑰是用來將 Operational Insights 代理程式連線至工作區。</span><span class="sxs-lookup"><span data-stu-id="b0a51-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="b0a51-108">示例</span><span class="sxs-lookup"><span data-stu-id="b0a51-108">EXAMPLES</span></span>

### <span data-ttu-id="b0a51-109">範例1：依工作區名稱取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="b0a51-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="b0a51-110">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b0a51-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="b0a51-111">範例2：使用管線取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="b0a51-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="b0a51-112">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將工作區傳送到 **AzureRmOperationalInsightsWorkspaceSharedKeys** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b0a51-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="b0a51-113">此命令會取得該工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="b0a51-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="b0a51-114">參數</span><span class="sxs-lookup"><span data-stu-id="b0a51-114">PARAMETERS</span></span>

### <span data-ttu-id="b0a51-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0a51-115">-DefaultProfile</span></span>
<span data-ttu-id="b0a51-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b0a51-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a51-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b0a51-117">-Name</span></span>
<span data-ttu-id="b0a51-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="b0a51-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b0a51-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0a51-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0a51-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b0a51-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="b0a51-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a51-121">CommonParameters</span></span>
<span data-ttu-id="b0a51-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b0a51-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a51-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b0a51-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a51-124">輸入</span><span class="sxs-lookup"><span data-stu-id="b0a51-124">INPUTS</span></span>

### <span data-ttu-id="b0a51-125">System.object</span><span class="sxs-lookup"><span data-stu-id="b0a51-125">System.String</span></span>

## <span data-ttu-id="b0a51-126">輸出</span><span class="sxs-lookup"><span data-stu-id="b0a51-126">OUTPUTS</span></span>

### <span data-ttu-id="b0a51-127">PSWorkspaceKeys 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="b0a51-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="b0a51-128">筆記</span><span class="sxs-lookup"><span data-stu-id="b0a51-128">NOTES</span></span>

## <span data-ttu-id="b0a51-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="b0a51-129">RELATED LINKS</span></span>

[<span data-ttu-id="b0a51-130">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0a51-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="b0a51-131">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b0a51-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


