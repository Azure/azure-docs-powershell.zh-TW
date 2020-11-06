---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 884d2a4168a4ce9efd27a6ae46387dae048f9ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449582"
---
# <span data-ttu-id="92620-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="92620-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="92620-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92620-102">SYNOPSIS</span></span>
<span data-ttu-id="92620-103">取得工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="92620-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92620-104">句法</span><span class="sxs-lookup"><span data-stu-id="92620-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92620-105">說明</span><span class="sxs-lookup"><span data-stu-id="92620-105">DESCRIPTION</span></span>
<span data-ttu-id="92620-106">**AzureRmOperationalInsightsWorkspaceSharedKeys** Cmdlet 會列出工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="92620-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="92620-107">金鑰是用來將 Operational Insights 代理程式連線至工作區。</span><span class="sxs-lookup"><span data-stu-id="92620-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="92620-108">示例</span><span class="sxs-lookup"><span data-stu-id="92620-108">EXAMPLES</span></span>

### <span data-ttu-id="92620-109">範例1：依工作區名稱取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="92620-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="92620-110">這個命令會取得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 之工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="92620-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="92620-111">範例2：使用管線取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="92620-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="92620-112">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後將工作區傳送到 **AzureRmOperationalInsightsWorkspaceSharedKeys** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92620-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="92620-113">此命令會取得該工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="92620-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="92620-114">參數</span><span class="sxs-lookup"><span data-stu-id="92620-114">PARAMETERS</span></span>

### <span data-ttu-id="92620-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="92620-115">-Name</span></span>
<span data-ttu-id="92620-116">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="92620-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="92620-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92620-117">-ResourceGroupName</span></span>
<span data-ttu-id="92620-118">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92620-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="92620-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92620-119">-DefaultProfile</span></span>
<span data-ttu-id="92620-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92620-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92620-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92620-121">CommonParameters</span></span>
<span data-ttu-id="92620-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92620-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92620-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="92620-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92620-124">輸入</span><span class="sxs-lookup"><span data-stu-id="92620-124">INPUTS</span></span>

## <span data-ttu-id="92620-125">輸出</span><span class="sxs-lookup"><span data-stu-id="92620-125">OUTPUTS</span></span>

### <span data-ttu-id="92620-126">PSWorkspaceKeys 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="92620-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="92620-127">筆記</span><span class="sxs-lookup"><span data-stu-id="92620-127">NOTES</span></span>

## <span data-ttu-id="92620-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="92620-128">RELATED LINKS</span></span>

[<span data-ttu-id="92620-129">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="92620-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="92620-130">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="92620-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


