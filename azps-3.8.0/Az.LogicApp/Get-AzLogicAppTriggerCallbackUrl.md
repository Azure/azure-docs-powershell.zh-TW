---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965790"
---
# <span data-ttu-id="3ea2c-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="3ea2c-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="3ea2c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ea2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea2c-103">取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="3ea2c-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ea2c-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ea2c-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ea2c-105">DESCRIPTION</span></span>
<span data-ttu-id="3ea2c-106">**AzLogicAppTriggerCallbackUrl** Cmdlet 會從資源群組取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="3ea2c-107">這個 Cmdlet 會傳回代表回呼 URL 的 **WorkflowTriggerCallbackUrl** 物件。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="3ea2c-108">指定資源群組名稱、邏輯 app 名稱及觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="3ea2c-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3ea2c-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3ea2c-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3ea2c-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3ea2c-113">示例</span><span class="sxs-lookup"><span data-stu-id="3ea2c-113">EXAMPLES</span></span>

### <span data-ttu-id="3ea2c-114">範例1：取得邏輯 App 觸發程式回撥 URL</span><span class="sxs-lookup"><span data-stu-id="3ea2c-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="3ea2c-115">這個命令會取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="3ea2c-116">參數</span><span class="sxs-lookup"><span data-stu-id="3ea2c-116">PARAMETERS</span></span>

### <span data-ttu-id="3ea2c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ea2c-117">-DefaultProfile</span></span>
<span data-ttu-id="3ea2c-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3ea2c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ea2c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ea2c-119">-Name</span></span>
<span data-ttu-id="3ea2c-120">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-120">Specifies the name of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ea2c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ea2c-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ea2c-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3ea2c-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="3ea2c-123">-TriggerName</span></span>
<span data-ttu-id="3ea2c-124">指定觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="3ea2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea2c-125">CommonParameters</span></span>
<span data-ttu-id="3ea2c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea2c-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea2c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="3ea2c-128">INPUTS</span></span>

### <span data-ttu-id="3ea2c-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3ea2c-129">System.String</span></span>

## <span data-ttu-id="3ea2c-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3ea2c-130">OUTPUTS</span></span>

### <span data-ttu-id="3ea2c-131">WorkflowTriggerCallbackUrl 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="3ea2c-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="3ea2c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3ea2c-132">NOTES</span></span>

## <span data-ttu-id="3ea2c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ea2c-133">RELATED LINKS</span></span>

[<span data-ttu-id="3ea2c-134">AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="3ea2c-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


