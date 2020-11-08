---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 3D4E44E3-0B55-4699-944F-412EE80CEEEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountSchema.md
ms.openlocfilehash: c43bfb5fd43df92d6b8d1674b4a856829b3258d8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139149"
---
# <span data-ttu-id="6f156-101">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6f156-101">Set-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="6f156-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f156-102">SYNOPSIS</span></span>
<span data-ttu-id="6f156-103">修改整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="6f156-103">Modifies an integration account schema.</span></span>

## <span data-ttu-id="6f156-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f156-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6f156-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f156-105">DESCRIPTION</span></span>
<span data-ttu-id="6f156-106">**AzIntegrationAccountSchema** Cmdlet 會修改整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="6f156-106">The **Set-AzIntegrationAccountSchema** cmdlet modifies an integration account schema.</span></span>
<span data-ttu-id="6f156-107">這個 Cmdlet 會傳回代表整合帳戶架構的物件。</span><span class="sxs-lookup"><span data-stu-id="6f156-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="6f156-108">指定整合帳戶名稱、資源群組名稱和架構名稱。</span><span class="sxs-lookup"><span data-stu-id="6f156-108">Specify the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="6f156-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="6f156-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6f156-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="6f156-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6f156-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="6f156-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6f156-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="6f156-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6f156-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="6f156-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6f156-114">示例</span><span class="sxs-lookup"><span data-stu-id="6f156-114">EXAMPLES</span></span>

### <span data-ttu-id="6f156-115">範例1：修改整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="6f156-115">Example 1: Modify an integration account schema</span></span>
```
PS C:\>Set-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema43
Name        : IntegrationAccountSchema43
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="6f156-116">這個命令會修改名為 IntegrationAccountSchema43 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="6f156-116">This command modifies the integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="6f156-117">參數</span><span class="sxs-lookup"><span data-stu-id="6f156-117">PARAMETERS</span></span>

### <span data-ttu-id="6f156-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="6f156-118">-ContentType</span></span>
<span data-ttu-id="6f156-119">指定整合帳戶架構的內容類型。</span><span class="sxs-lookup"><span data-stu-id="6f156-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="6f156-120">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="6f156-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="6f156-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f156-121">-DefaultProfile</span></span>
<span data-ttu-id="6f156-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6f156-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f156-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6f156-123">-Force</span></span>
<span data-ttu-id="6f156-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6f156-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f156-125">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6f156-125">-Metadata</span></span>
<span data-ttu-id="6f156-126">指定架構的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="6f156-126">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="6f156-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f156-127">-Name</span></span>
<span data-ttu-id="6f156-128">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f156-128">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="6f156-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f156-129">-ResourceGroupName</span></span>
<span data-ttu-id="6f156-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f156-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6f156-131">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="6f156-131">-SchemaDefinition</span></span>
<span data-ttu-id="6f156-132">指定整合帳戶架構的定義物件。</span><span class="sxs-lookup"><span data-stu-id="6f156-132">Specifies a definition object for integration account schema.</span></span>

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

### <span data-ttu-id="6f156-133">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="6f156-133">-SchemaFilePath</span></span>
<span data-ttu-id="6f156-134">指定整合帳戶架構之定義的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="6f156-134">Specifies the file path of a definition for the integration account schema.</span></span>

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

### <span data-ttu-id="6f156-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6f156-135">-SchemaName</span></span>
<span data-ttu-id="6f156-136">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f156-136">Specifies the name of the integration account schema.</span></span>

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

### <span data-ttu-id="6f156-137">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="6f156-137">-SchemaType</span></span>
<span data-ttu-id="6f156-138">指定整合帳戶架構的類型。</span><span class="sxs-lookup"><span data-stu-id="6f156-138">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="6f156-139">此參數支援 Xml 作為類型。</span><span class="sxs-lookup"><span data-stu-id="6f156-139">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="6f156-140">-確認</span><span class="sxs-lookup"><span data-stu-id="6f156-140">-Confirm</span></span>
<span data-ttu-id="6f156-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f156-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f156-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f156-142">-WhatIf</span></span>
<span data-ttu-id="6f156-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f156-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f156-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f156-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f156-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f156-145">CommonParameters</span></span>
<span data-ttu-id="6f156-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f156-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f156-147">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f156-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f156-148">輸入</span><span class="sxs-lookup"><span data-stu-id="6f156-148">INPUTS</span></span>

### <span data-ttu-id="6f156-149">System.object</span><span class="sxs-lookup"><span data-stu-id="6f156-149">System.String</span></span>

## <span data-ttu-id="6f156-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6f156-150">OUTPUTS</span></span>

### <span data-ttu-id="6f156-151">IntegrationAccountSchema 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="6f156-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="6f156-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6f156-152">NOTES</span></span>

## <span data-ttu-id="6f156-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f156-153">RELATED LINKS</span></span>

[<span data-ttu-id="6f156-154">AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6f156-154">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="6f156-155">新-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6f156-155">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="6f156-156">移除-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="6f156-156">Remove-AzIntegrationAccountSchema</span></span>](./Remove-AzIntegrationAccountSchema.md)

