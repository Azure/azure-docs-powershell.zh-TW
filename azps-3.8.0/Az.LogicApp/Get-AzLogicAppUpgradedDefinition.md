---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B7FED447-C398-47D7-AF1B-A3E4FDAD0B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicappupgradeddefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppUpgradedDefinition.md
ms.openlocfilehash: 2c0eb437aaa8a280b970e9c2a210b37b8fbce2d8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93965789"
---
# <span data-ttu-id="551c5-101">Get-AzLogicAppUpgradedDefinition</span><span class="sxs-lookup"><span data-stu-id="551c5-101">Get-AzLogicAppUpgradedDefinition</span></span>

## <span data-ttu-id="551c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="551c5-102">SYNOPSIS</span></span>
<span data-ttu-id="551c5-103">取得邏輯 app 的升級定義。</span><span class="sxs-lookup"><span data-stu-id="551c5-103">Gets the upgraded definition for a logic app.</span></span>

## <span data-ttu-id="551c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="551c5-104">SYNTAX</span></span>

```
Get-AzLogicAppUpgradedDefinition -ResourceGroupName <String> -Name <String> -TargetSchemaVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="551c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="551c5-105">DESCRIPTION</span></span>
<span data-ttu-id="551c5-106">**AzLogicAppUpgradedDefinition** Cmdlet 會從資源群組取得架構版本與邏輯 app 的升級定義。</span><span class="sxs-lookup"><span data-stu-id="551c5-106">The **Get-AzLogicAppUpgradedDefinition** cmdlet gets the upgraded definition for the schema version and logic app from a resource group.</span></span>
<span data-ttu-id="551c5-107">這個 Cmdlet 會傳回代表已升級之邏輯 app 之定義的物件。</span><span class="sxs-lookup"><span data-stu-id="551c5-107">This cmdlet returns an object that represents the definition of the upgraded logic app.</span></span>
<span data-ttu-id="551c5-108">指定資源群組名稱、邏輯 app 名稱和目標架構版本。</span><span class="sxs-lookup"><span data-stu-id="551c5-108">Specify the resource group name, logic app name, and target schema version.</span></span>
<span data-ttu-id="551c5-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="551c5-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="551c5-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="551c5-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="551c5-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="551c5-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="551c5-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="551c5-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="551c5-113">示例</span><span class="sxs-lookup"><span data-stu-id="551c5-113">EXAMPLES</span></span>

### <span data-ttu-id="551c5-114">範例1：取得邏輯 app 已升級的定義</span><span class="sxs-lookup"><span data-stu-id="551c5-114">Example 1: Get a logic app upgraded definition</span></span>
```
PS C:\>$UpgradedDefinition = Get-AzLogicAppUpgradedDefinition -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -TargetSchemaVersion "2016-06-01"
$UpgradedDefinition.ToString()
{

  "$schema": "http://schema.management.azure.com/providers/Microsoft.Logic/schemas/2016-06-01/workflowdefinition.json#",

  "contentVersion": "1.0.0.0",

  "parameters": {},

  "triggers": {

    "httpTrigger": {

      "recurrence": {

        "frequency": "Hour",

        "interval": 1

      },

      "type": "Http",

      "inputs": {

        "method": "GET",

        "uri": "http://www.bing.com"

      },

      "conditions": [

        {

          "expression": "@bool('true')" 

        }

      ] 

    },

    "manualTrigger": {

      "type": "Request",

      "kind": "Http"

    }

  },

  "actions": {

    "httpScope": {

      "actions": {

        "http": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    },

    "http1Scope": {

      "actions": {

        "http1": {

          "runAfter": {},

          "type": "Http",

          "inputs": {

            "method": "GET",

            "uri": "http://www.bing.com"

          }

        }

      },

      "runAfter": {},

      "else": {

        "actions": {}

      },

      "expression": "@bool('true')", 

      "type": "If"

    }

  },

  "outputs": {

    "output1": {

      "type": "String",

      "value": "true"

    }

  }

}
```

<span data-ttu-id="551c5-115">第一個命令會取得已升級至指定目標架構版本之邏輯 app 的定義。</span><span class="sxs-lookup"><span data-stu-id="551c5-115">The first command gets the definition for the logic app upgraded to the specified target schema version.</span></span>
<span data-ttu-id="551c5-116">該命令會將定義儲存在 $UpgradedDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="551c5-116">The command stores the definition in the $UpgradedDefinition variable.</span></span>
<span data-ttu-id="551c5-117">第二個命令會將 $UpgradedDefinition 的內容顯示為一個字串。</span><span class="sxs-lookup"><span data-stu-id="551c5-117">The second command displays the contents of $UpgradedDefinition as a string.</span></span>

## <span data-ttu-id="551c5-118">參數</span><span class="sxs-lookup"><span data-stu-id="551c5-118">PARAMETERS</span></span>

### <span data-ttu-id="551c5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551c5-119">-DefaultProfile</span></span>
<span data-ttu-id="551c5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="551c5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="551c5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="551c5-121">-Name</span></span>
<span data-ttu-id="551c5-122">指定邏輯應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="551c5-122">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="551c5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551c5-123">-ResourceGroupName</span></span>
<span data-ttu-id="551c5-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="551c5-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="551c5-125">-TargetSchemaVersion</span><span class="sxs-lookup"><span data-stu-id="551c5-125">-TargetSchemaVersion</span></span>
<span data-ttu-id="551c5-126">指定定義的目標架構版本。</span><span class="sxs-lookup"><span data-stu-id="551c5-126">Specifies the target schema version of the definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="551c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551c5-127">CommonParameters</span></span>
<span data-ttu-id="551c5-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="551c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551c5-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="551c5-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551c5-130">輸入</span><span class="sxs-lookup"><span data-stu-id="551c5-130">INPUTS</span></span>

### <span data-ttu-id="551c5-131">System.object</span><span class="sxs-lookup"><span data-stu-id="551c5-131">System.String</span></span>

## <span data-ttu-id="551c5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="551c5-132">OUTPUTS</span></span>

### <span data-ttu-id="551c5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="551c5-133">System.Object</span></span>

## <span data-ttu-id="551c5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="551c5-134">NOTES</span></span>

## <span data-ttu-id="551c5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="551c5-135">RELATED LINKS</span></span>

[<span data-ttu-id="551c5-136">AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="551c5-136">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)


