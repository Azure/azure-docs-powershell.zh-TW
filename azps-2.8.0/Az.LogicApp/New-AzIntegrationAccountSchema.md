---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountSchema.md
ms.openlocfilehash: 70f3e36daf14b4ee2d500724785db9de59a58e1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611987"
---
# <span data-ttu-id="a5da1-101">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a5da1-101">New-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="a5da1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5da1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5da1-103">建立整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="a5da1-103">Creates an integration account schema.</span></span>

## <span data-ttu-id="a5da1-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5da1-104">SYNTAX</span></span>

```
New-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5da1-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5da1-105">DESCRIPTION</span></span>
<span data-ttu-id="a5da1-106">**新的-AzIntegrationAccountSchema** Cmdlet 會建立整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="a5da1-106">The **New-AzIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="a5da1-107">這個 Cmdlet 會傳回代表整合帳戶架構的物件。</span><span class="sxs-lookup"><span data-stu-id="a5da1-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="a5da1-108">指定整合帳戶名稱、資源組名稱、架構名稱和架構定義。</span><span class="sxs-lookup"><span data-stu-id="a5da1-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>
<span data-ttu-id="a5da1-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="a5da1-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="a5da1-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="a5da1-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a5da1-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="a5da1-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a5da1-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="a5da1-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a5da1-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="a5da1-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a5da1-114">示例</span><span class="sxs-lookup"><span data-stu-id="a5da1-114">EXAMPLES</span></span>

### <span data-ttu-id="a5da1-115">範例1：建立整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="a5da1-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="a5da1-116">這個命令會在指定的資源群組中建立名為 IntegrationAccountSchema1 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="a5da1-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="a5da1-117">參數</span><span class="sxs-lookup"><span data-stu-id="a5da1-117">PARAMETERS</span></span>

### <span data-ttu-id="a5da1-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="a5da1-118">-ContentType</span></span>
<span data-ttu-id="a5da1-119">指定整合帳戶架構的內容類型。</span><span class="sxs-lookup"><span data-stu-id="a5da1-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="a5da1-120">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="a5da1-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="a5da1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5da1-121">-DefaultProfile</span></span>
<span data-ttu-id="a5da1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a5da1-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5da1-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="a5da1-123">-Metadata</span></span>
<span data-ttu-id="a5da1-124">指定架構的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="a5da1-124">Specifies a metadata object for the schema.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5da1-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5da1-125">-Name</span></span>
<span data-ttu-id="a5da1-126">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5da1-126">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5da1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5da1-127">-ResourceGroupName</span></span>
<span data-ttu-id="a5da1-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5da1-128">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a5da1-129">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="a5da1-129">-SchemaDefinition</span></span>
<span data-ttu-id="a5da1-130">指定整合帳戶架構的定義物件。</span><span class="sxs-lookup"><span data-stu-id="a5da1-130">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="a5da1-131">請指定此參數或 *SchemaFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5da1-131">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="a5da1-132">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="a5da1-132">-SchemaFilePath</span></span>
<span data-ttu-id="a5da1-133">指定整合帳戶架構之定義的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="a5da1-133">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="a5da1-134">請指定此參數或 *SchemaDefinition* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5da1-134">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="a5da1-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a5da1-135">-SchemaName</span></span>
<span data-ttu-id="a5da1-136">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5da1-136">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="a5da1-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="a5da1-137">-SchemaType</span></span>
<span data-ttu-id="a5da1-138">指定整合帳戶架構的類型。</span><span class="sxs-lookup"><span data-stu-id="a5da1-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="a5da1-139">此參數支援 Xml 作為類型。</span><span class="sxs-lookup"><span data-stu-id="a5da1-139">This parameter supports Xml as the type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xml

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5da1-140">-確認</span><span class="sxs-lookup"><span data-stu-id="a5da1-140">-Confirm</span></span>
<span data-ttu-id="a5da1-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5da1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5da1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5da1-142">-WhatIf</span></span>
<span data-ttu-id="a5da1-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5da1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5da1-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5da1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5da1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5da1-145">CommonParameters</span></span>
<span data-ttu-id="a5da1-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5da1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5da1-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5da1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5da1-148">輸入</span><span class="sxs-lookup"><span data-stu-id="a5da1-148">INPUTS</span></span>

### <span data-ttu-id="a5da1-149">System.object</span><span class="sxs-lookup"><span data-stu-id="a5da1-149">System.String</span></span>

## <span data-ttu-id="a5da1-150">輸出</span><span class="sxs-lookup"><span data-stu-id="a5da1-150">OUTPUTS</span></span>

### <span data-ttu-id="a5da1-151">IntegrationAccountSchema 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="a5da1-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="a5da1-152">筆記</span><span class="sxs-lookup"><span data-stu-id="a5da1-152">NOTES</span></span>

## <span data-ttu-id="a5da1-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5da1-153">RELATED LINKS</span></span>

[<span data-ttu-id="a5da1-154">AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a5da1-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="a5da1-155">移除-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a5da1-155">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

[<span data-ttu-id="a5da1-156">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="a5da1-156">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)

