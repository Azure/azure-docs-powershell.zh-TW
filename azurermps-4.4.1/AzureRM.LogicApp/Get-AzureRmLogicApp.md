---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 891f7fcd50281f5dab9b8d4eaf9f1bd842fbc85e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446767"
---
# <span data-ttu-id="f2aa2-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f2aa2-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="f2aa2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="f2aa2-103">從資源群組取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2aa2-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2aa2-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2aa2-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2aa2-105">DESCRIPTION</span></span>
<span data-ttu-id="f2aa2-106">**AzureRmLogicApp** Cmdlet 會取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="f2aa2-107">這個 Cmdlet 會傳回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="f2aa2-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f2aa2-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f2aa2-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f2aa2-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f2aa2-112">示例</span><span class="sxs-lookup"><span data-stu-id="f2aa2-112">EXAMPLES</span></span>

### <span data-ttu-id="f2aa2-113">範例1：從資源群組取得邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="f2aa2-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="f2aa2-114">這個命令會從名為 ResourceGroup11 的資源群組中取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f2aa2-115">參數</span><span class="sxs-lookup"><span data-stu-id="f2aa2-115">PARAMETERS</span></span>

### <span data-ttu-id="f2aa2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2aa2-116">-Name</span></span>
<span data-ttu-id="f2aa2-117">指定此 Cmdlet 取得的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-117">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2aa2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2aa2-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2aa2-119">指定此 Cmdlet 取得邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-119">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2aa2-120">-版本</span><span class="sxs-lookup"><span data-stu-id="f2aa2-120">-Version</span></span>
<span data-ttu-id="f2aa2-121">指定邏輯 app 的版本。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-121">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2aa2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2aa2-122">-DefaultProfile</span></span>
<span data-ttu-id="f2aa2-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2aa2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2aa2-124">CommonParameters</span></span>
<span data-ttu-id="f2aa2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2aa2-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2aa2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2aa2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f2aa2-127">INPUTS</span></span>

## <span data-ttu-id="f2aa2-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f2aa2-128">OUTPUTS</span></span>

### <span data-ttu-id="f2aa2-129">[Azure. 管理]。工作流程</span><span class="sxs-lookup"><span data-stu-id="f2aa2-129">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="f2aa2-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f2aa2-130">NOTES</span></span>

## <span data-ttu-id="f2aa2-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2aa2-131">RELATED LINKS</span></span>

[<span data-ttu-id="f2aa2-132">新-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f2aa2-132">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="f2aa2-133">移除-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f2aa2-133">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="f2aa2-134">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f2aa2-134">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="f2aa2-135">開始-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="f2aa2-135">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


