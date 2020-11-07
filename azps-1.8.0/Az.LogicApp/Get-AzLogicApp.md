---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: 531a863703ffc0a594f09bade4b9c4044966024a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787157"
---
# <span data-ttu-id="85ec2-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="85ec2-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="85ec2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="85ec2-103">從資源群組取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="85ec2-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="85ec2-104">句法</span><span class="sxs-lookup"><span data-stu-id="85ec2-104">SYNTAX</span></span>

### <span data-ttu-id="85ec2-105">ListWorkflows (預設) </span><span class="sxs-lookup"><span data-stu-id="85ec2-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85ec2-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="85ec2-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85ec2-107">說明</span><span class="sxs-lookup"><span data-stu-id="85ec2-107">DESCRIPTION</span></span>
<span data-ttu-id="85ec2-108">**AzLogicApp** Cmdlet 會取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="85ec2-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="85ec2-109">這個 Cmdlet 會傳回 **工作流程** 物件。</span><span class="sxs-lookup"><span data-stu-id="85ec2-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="85ec2-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="85ec2-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="85ec2-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="85ec2-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="85ec2-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="85ec2-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="85ec2-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="85ec2-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="85ec2-114">示例</span><span class="sxs-lookup"><span data-stu-id="85ec2-114">EXAMPLES</span></span>

### <span data-ttu-id="85ec2-115">範例1：從資源群組取得邏輯應用程式</span><span class="sxs-lookup"><span data-stu-id="85ec2-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="85ec2-116">這個命令會從名為 ResourceGroup11 的資源群組中取得邏輯 app。</span><span class="sxs-lookup"><span data-stu-id="85ec2-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="85ec2-117">參數</span><span class="sxs-lookup"><span data-stu-id="85ec2-117">PARAMETERS</span></span>

### <span data-ttu-id="85ec2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ec2-118">-DefaultProfile</span></span>
<span data-ttu-id="85ec2-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="85ec2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85ec2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="85ec2-120">-Name</span></span>
<span data-ttu-id="85ec2-121">指定此 Cmdlet 取得的邏輯 app 名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec2-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ec2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ec2-122">-ResourceGroupName</span></span>
<span data-ttu-id="85ec2-123">指定此 Cmdlet 取得邏輯 app 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85ec2-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85ec2-124">-版本</span><span class="sxs-lookup"><span data-stu-id="85ec2-124">-Version</span></span>
<span data-ttu-id="85ec2-125">指定邏輯 app 的版本。</span><span class="sxs-lookup"><span data-stu-id="85ec2-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ec2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ec2-126">CommonParameters</span></span>
<span data-ttu-id="85ec2-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85ec2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ec2-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85ec2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ec2-129">輸入</span><span class="sxs-lookup"><span data-stu-id="85ec2-129">INPUTS</span></span>

### <span data-ttu-id="85ec2-130">System.object</span><span class="sxs-lookup"><span data-stu-id="85ec2-130">System.String</span></span>

## <span data-ttu-id="85ec2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="85ec2-131">OUTPUTS</span></span>

### <span data-ttu-id="85ec2-132">[Azure. 管理]。工作流程</span><span class="sxs-lookup"><span data-stu-id="85ec2-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="85ec2-133">WorkflowVersion 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="85ec2-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="85ec2-134">筆記</span><span class="sxs-lookup"><span data-stu-id="85ec2-134">NOTES</span></span>

## <span data-ttu-id="85ec2-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="85ec2-135">RELATED LINKS</span></span>

[<span data-ttu-id="85ec2-136">新-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="85ec2-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="85ec2-137">移除-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="85ec2-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="85ec2-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="85ec2-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="85ec2-139">開始-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="85ec2-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


