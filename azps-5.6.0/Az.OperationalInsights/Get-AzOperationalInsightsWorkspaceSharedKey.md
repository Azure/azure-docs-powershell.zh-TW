---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 2cf7f548db74a7c7393fcd52bb7183c54f5f4e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914705"
---
# <span data-ttu-id="0eccd-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="0eccd-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="0eccd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0eccd-102">SYNOPSIS</span></span>
<span data-ttu-id="0eccd-103">獲得工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0eccd-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="0eccd-104">語法</span><span class="sxs-lookup"><span data-stu-id="0eccd-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0eccd-105">描述</span><span class="sxs-lookup"><span data-stu-id="0eccd-105">DESCRIPTION</span></span>
<span data-ttu-id="0eccd-106">**Get-AzOperationalInsightsWorkspaceSharedKey** Cmdlet 會列出工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0eccd-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="0eccd-107">這些金鑰可用來將營運深入資訊代理程式連接到工作區。</span><span class="sxs-lookup"><span data-stu-id="0eccd-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="0eccd-108">例子</span><span class="sxs-lookup"><span data-stu-id="0eccd-108">EXAMPLES</span></span>

### <span data-ttu-id="0eccd-109">範例 1：根據工作區名稱取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="0eccd-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0eccd-110">此命令會獲得名為 ContosoResourceGroup 之資源群組中名為 MyWorkspace 的工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0eccd-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0eccd-111">範例 2：使用管線取得共用金鑰</span><span class="sxs-lookup"><span data-stu-id="0eccd-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="0eccd-112">此命令會使用 Get-AzOperationalInsightsWorkspace Cmdlet 取得名為 MyWorkspace 的工作區，然後將工作區傳遞至 **Get-AzOperationalInsightsWorkspaceSharedKey** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0eccd-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="0eccd-113">該命令會獲得該工作區的共用金鑰。</span><span class="sxs-lookup"><span data-stu-id="0eccd-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="0eccd-114">參數</span><span class="sxs-lookup"><span data-stu-id="0eccd-114">PARAMETERS</span></span>

### <span data-ttu-id="0eccd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eccd-115">-DefaultProfile</span></span>
<span data-ttu-id="0eccd-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="0eccd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0eccd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0eccd-117">-Name</span></span>
<span data-ttu-id="0eccd-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="0eccd-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0eccd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eccd-119">-ResourceGroupName</span></span>
<span data-ttu-id="0eccd-120">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0eccd-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0eccd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eccd-121">CommonParameters</span></span>
<span data-ttu-id="0eccd-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0eccd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eccd-123">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0eccd-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eccd-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0eccd-124">INPUTS</span></span>

### <span data-ttu-id="0eccd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="0eccd-125">System.String</span></span>

## <span data-ttu-id="0eccd-126">輸出</span><span class="sxs-lookup"><span data-stu-id="0eccd-126">OUTPUTS</span></span>

### <span data-ttu-id="0eccd-127">Microsoft.Azure.Commands.OperationalInsights.models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="0eccd-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="0eccd-128">筆記</span><span class="sxs-lookup"><span data-stu-id="0eccd-128">NOTES</span></span>

## <span data-ttu-id="0eccd-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0eccd-129">RELATED LINKS</span></span>

[<span data-ttu-id="0eccd-130">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0eccd-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0eccd-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0eccd-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


