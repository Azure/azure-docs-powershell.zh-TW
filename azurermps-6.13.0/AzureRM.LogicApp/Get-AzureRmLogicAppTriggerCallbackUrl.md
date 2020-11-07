---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: b1b45fc6d06ec77d3e94254ed044a0a5a6f39406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625282"
---
# <span data-ttu-id="b065b-101">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b065b-101">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="b065b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b065b-102">SYNOPSIS</span></span>
<span data-ttu-id="b065b-103">取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="b065b-103">Gets a Logic App trigger callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b065b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b065b-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b065b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b065b-105">DESCRIPTION</span></span>
<span data-ttu-id="b065b-106">**AzureRmLogicAppTriggerCallbackUrl** Cmdlet 會從資源群組取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="b065b-106">The **Get-AzureRmLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="b065b-107">這個 Cmdlet 會傳回代表回呼 URL 的 **WorkflowTriggerCallbackUrl** 物件。</span><span class="sxs-lookup"><span data-stu-id="b065b-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="b065b-108">指定資源群組名稱、邏輯 app 名稱及觸發程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b065b-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="b065b-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b065b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b065b-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b065b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b065b-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b065b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b065b-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b065b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b065b-113">示例</span><span class="sxs-lookup"><span data-stu-id="b065b-113">EXAMPLES</span></span>

### <span data-ttu-id="b065b-114">範例1：取得邏輯 App 觸發程式回撥 URL</span><span class="sxs-lookup"><span data-stu-id="b065b-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="b065b-115">這個命令會取得邏輯 App 觸發程式回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="b065b-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="b065b-116">參數</span><span class="sxs-lookup"><span data-stu-id="b065b-116">PARAMETERS</span></span>

### <span data-ttu-id="b065b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b065b-117">-DefaultProfile</span></span>
<span data-ttu-id="b065b-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b065b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b065b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b065b-119">-Name</span></span>
<span data-ttu-id="b065b-120">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b065b-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="b065b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b065b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b065b-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b065b-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b065b-123">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="b065b-123">-TriggerName</span></span>
<span data-ttu-id="b065b-124">指定觸發程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="b065b-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="b065b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b065b-125">CommonParameters</span></span>
<span data-ttu-id="b065b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b065b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b065b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b065b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b065b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b065b-128">INPUTS</span></span>

### <span data-ttu-id="b065b-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b065b-129">System.String</span></span>

## <span data-ttu-id="b065b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b065b-130">OUTPUTS</span></span>

### <span data-ttu-id="b065b-131">WorkflowTriggerCallbackUrl 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="b065b-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="b065b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b065b-132">NOTES</span></span>

## <span data-ttu-id="b065b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b065b-133">RELATED LINKS</span></span>

[<span data-ttu-id="b065b-134">AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b065b-134">Get-AzureRmIntegrationAccountCallbackUrl</span></span>](./Get-AzureRmIntegrationAccountCallbackUrl.md)


