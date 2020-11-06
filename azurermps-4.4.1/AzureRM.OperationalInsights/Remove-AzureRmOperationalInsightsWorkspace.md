---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 3f7ed1a36cc95296ee7fdeec45c5039063032d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446699"
---
# <span data-ttu-id="73e94-101">Remove-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="73e94-101">Remove-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="73e94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="73e94-102">SYNOPSIS</span></span>
<span data-ttu-id="73e94-103">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="73e94-103">Removes a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73e94-104">句法</span><span class="sxs-lookup"><span data-stu-id="73e94-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e94-105">說明</span><span class="sxs-lookup"><span data-stu-id="73e94-105">DESCRIPTION</span></span>
<span data-ttu-id="73e94-106">**AzureRmOperationalInsightsWorkspace** Cmdlet 會刪除現有的工作區。</span><span class="sxs-lookup"><span data-stu-id="73e94-106">The **Remove-AzureRmOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="73e94-107">如果此工作區是在建立期間透過 [ *CustomerId* ] 參數連結至現有的帳戶，原始帳戶不會在 Operational Insights 入口網站中刪除。</span><span class="sxs-lookup"><span data-stu-id="73e94-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="73e94-108">示例</span><span class="sxs-lookup"><span data-stu-id="73e94-108">EXAMPLES</span></span>

### <span data-ttu-id="73e94-109">範例1：依名稱移除工作區</span><span class="sxs-lookup"><span data-stu-id="73e94-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="73e94-110">這個命令會從名為 ContosoResourceGroup 的資源群組中移除名為 MyWorkspace 的工作區。</span><span class="sxs-lookup"><span data-stu-id="73e94-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="73e94-111">範例2：使用管線移除工作區，而不進行確認</span><span class="sxs-lookup"><span data-stu-id="73e94-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzureRmOperationalInsightsWorkspace -Force
```

<span data-ttu-id="73e94-112">這個命令會使用 Get-AzureRmOperationalInsightsWorkspace Cmdlet 來取得名為 MyWorkspace 的工作區，然後使用管線運算子將它傳送到 **Remove AzureRmOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73e94-112">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="73e94-113">由於已指定 *Force* 參數，因此在移除工作區前，命令不會提示您。</span><span class="sxs-lookup"><span data-stu-id="73e94-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="73e94-114">參數</span><span class="sxs-lookup"><span data-stu-id="73e94-114">PARAMETERS</span></span>

### <span data-ttu-id="73e94-115">-Force</span><span class="sxs-lookup"><span data-stu-id="73e94-115">-Force</span></span>
<span data-ttu-id="73e94-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="73e94-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e94-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="73e94-117">-Name</span></span>
<span data-ttu-id="73e94-118">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="73e94-118">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="73e94-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e94-119">-ResourceGroupName</span></span>
<span data-ttu-id="73e94-120">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="73e94-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="73e94-121">-確認</span><span class="sxs-lookup"><span data-stu-id="73e94-121">-Confirm</span></span>
<span data-ttu-id="73e94-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="73e94-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e94-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e94-123">-WhatIf</span></span>
<span data-ttu-id="73e94-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="73e94-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73e94-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="73e94-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e94-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e94-126">-DefaultProfile</span></span>
<span data-ttu-id="73e94-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="73e94-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e94-128">CommonParameters</span></span>
<span data-ttu-id="73e94-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="73e94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e94-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="73e94-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e94-131">輸入</span><span class="sxs-lookup"><span data-stu-id="73e94-131">INPUTS</span></span>

## <span data-ttu-id="73e94-132">輸出</span><span class="sxs-lookup"><span data-stu-id="73e94-132">OUTPUTS</span></span>

## <span data-ttu-id="73e94-133">筆記</span><span class="sxs-lookup"><span data-stu-id="73e94-133">NOTES</span></span>

## <span data-ttu-id="73e94-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="73e94-134">RELATED LINKS</span></span>

[<span data-ttu-id="73e94-135">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="73e94-135">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="73e94-136">AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="73e94-136">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


