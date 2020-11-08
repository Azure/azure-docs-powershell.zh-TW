---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6C16B04B-459A-4B2C-B7DF-AC4D16FF7281
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountSchema.md
ms.openlocfilehash: ed85c1fea8bd338b3dd4f2a9e82ee5aac3f3b52b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141611"
---
# <span data-ttu-id="9b713-101">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b713-101">Get-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="9b713-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b713-102">SYNOPSIS</span></span>
<span data-ttu-id="9b713-103">取得整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="9b713-103">Gets integration account schemas.</span></span>

## <span data-ttu-id="9b713-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b713-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountSchema [-ResourceGroupName <String>] [-Name <String>] [-SchemaName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b713-105">說明</span><span class="sxs-lookup"><span data-stu-id="9b713-105">DESCRIPTION</span></span>
<span data-ttu-id="9b713-106">**AzIntegrationAccountSchema** Cmdlet 會取得整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="9b713-106">The **Get-AzIntegrationAccountSchema** cmdlet gets integration account schemas.</span></span>
<span data-ttu-id="9b713-107">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="9b713-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="9b713-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="9b713-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9b713-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="9b713-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9b713-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="9b713-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9b713-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="9b713-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9b713-112">示例</span><span class="sxs-lookup"><span data-stu-id="9b713-112">EXAMPLES</span></span>

### <span data-ttu-id="9b713-113">範例1：取得整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="9b713-113">Example 1: Get an integration account schema</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
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

<span data-ttu-id="9b713-114">這個命令會取得名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="9b713-114">This command gets the integration account schema named IntegrationAccountSchema43.</span></span>

### <span data-ttu-id="9b713-115">範例2：取得資源群組的整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="9b713-115">Example 2: Get integration account schemas for a resource group</span></span>
```
PS C:\>Get-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="9b713-116">這個命令會取得名為 ResourceGroup11 之資源群組的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="9b713-116">This command gets the integration account schemas for the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="9b713-117">參數</span><span class="sxs-lookup"><span data-stu-id="9b713-117">PARAMETERS</span></span>

### <span data-ttu-id="9b713-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b713-118">-DefaultProfile</span></span>
<span data-ttu-id="9b713-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9b713-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b713-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b713-120">-Name</span></span>
<span data-ttu-id="9b713-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b713-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="9b713-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b713-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b713-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b713-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9b713-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9b713-124">-SchemaName</span></span>
<span data-ttu-id="9b713-125">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b713-125">Specifies the name of an integration account schema.</span></span>
<span data-ttu-id="9b713-126">指定架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b713-126">Specifies the name of a schema.</span></span>
<span data-ttu-id="9b713-127">.</span><span class="sxs-lookup"><span data-stu-id="9b713-127">.</span></span>

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

### <span data-ttu-id="9b713-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b713-128">CommonParameters</span></span>
<span data-ttu-id="9b713-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b713-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b713-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9b713-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b713-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9b713-131">INPUTS</span></span>

### <span data-ttu-id="9b713-132">System.object</span><span class="sxs-lookup"><span data-stu-id="9b713-132">System.String</span></span>

## <span data-ttu-id="9b713-133">輸出</span><span class="sxs-lookup"><span data-stu-id="9b713-133">OUTPUTS</span></span>

### <span data-ttu-id="9b713-134">IntegrationAccountSchema 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="9b713-134">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="9b713-135">筆記</span><span class="sxs-lookup"><span data-stu-id="9b713-135">NOTES</span></span>

## <span data-ttu-id="9b713-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b713-136">RELATED LINKS</span></span>

[<span data-ttu-id="9b713-137">新-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b713-137">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9b713-138">移除-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b713-138">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="9b713-139">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9b713-139">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


