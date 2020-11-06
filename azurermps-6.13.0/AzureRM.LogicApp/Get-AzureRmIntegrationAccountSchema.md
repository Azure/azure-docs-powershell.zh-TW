---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: 06aebcf21b7a9fb69887c8922343faf7867d796c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453727"
---
# <span data-ttu-id="524f8-101">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="524f8-101">Get-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="524f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="524f8-102">SYNOPSIS</span></span>
<span data-ttu-id="524f8-103">取得整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="524f8-103">Gets integration account schemas.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="524f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="524f8-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="524f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="524f8-105">DESCRIPTION</span></span>
<span data-ttu-id="524f8-106">**AzureRmIntegrationAccountSchema** Cmdlet 會取得整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="524f8-106">The **Get-AzureRmIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="524f8-107">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="524f8-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="524f8-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="524f8-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="524f8-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="524f8-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="524f8-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="524f8-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="524f8-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="524f8-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="524f8-112">示例</span><span class="sxs-lookup"><span data-stu-id="524f8-112">EXAMPLES</span></span>

### <span data-ttu-id="524f8-113">範例1：取得整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="524f8-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="524f8-114">這個命令會取得名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="524f8-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="524f8-115">範例2：取得資源群組的整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="524f8-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                   : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name                 : IntegrationAccountSchema43
Type                 : Microsoft.Logic/integrationAccounts/schemas
CreatedTime          : 3/25/2016 5:42:58 PM
ChangedTime          : 3/25/2016 5:42:58 PM
SchemaType           : Xml
ContentType          : 
ContentLink          : https://<baseurl>/integrationaccounts469af4f3cf4047b7ac3a08c87948ec5f/3839E_XML_INTEGRATIONACCOUNTSCHEMA43-5A86631F61F
                       14513AA1185A52C6B2874?sv=2014-02-14&sr=b&sig=<value>
ContentSize          : 7901
MetaData             :
```

<span data-ttu-id="524f8-116">這個命令會取得名為 ResourceGroup11 之資源群組的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="524f8-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="524f8-117">參數</span><span class="sxs-lookup"><span data-stu-id="524f8-117">PARAMETERS</span></span>

### <span data-ttu-id="524f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524f8-118">-DefaultProfile</span></span>
<span data-ttu-id="524f8-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="524f8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="524f8-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="524f8-120">-Name</span></span>
<span data-ttu-id="524f8-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="524f8-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="524f8-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524f8-122">-ResourceGroupName</span></span>
<span data-ttu-id="524f8-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="524f8-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="524f8-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="524f8-124">-SchemaName</span></span>
<span data-ttu-id="524f8-125">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="524f8-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="524f8-126">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="524f8-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="524f8-127">.</span><span class="sxs-lookup"><span data-stu-id="524f8-127">.</span></span>

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

### <span data-ttu-id="524f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524f8-128">CommonParameters</span></span>
<span data-ttu-id="524f8-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="524f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524f8-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="524f8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524f8-131">輸入</span><span class="sxs-lookup"><span data-stu-id="524f8-131">INPUTS</span></span>

### <span data-ttu-id="524f8-132">System.object</span><span class="sxs-lookup"><span data-stu-id="524f8-132">System.String</span></span>

## <span data-ttu-id="524f8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="524f8-133">OUTPUTS</span></span>

### <span data-ttu-id="524f8-134">IntegrationAccountSchema 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="524f8-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="524f8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="524f8-135">NOTES</span></span>

## <span data-ttu-id="524f8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="524f8-136">RELATED LINKS</span></span>

[<span data-ttu-id="524f8-137">新-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="524f8-137">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="524f8-138">移除-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="524f8-138">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="524f8-139">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="524f8-139">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)

