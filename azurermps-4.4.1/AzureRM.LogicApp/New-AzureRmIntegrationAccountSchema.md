---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 91FFBEE9-A488-49ED-8C6C-2DE891CE0749
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a9320219e05e61bcd77f15dd526ad45794bd45bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457575"
---
# <span data-ttu-id="cc1d6-101">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cc1d6-101">New-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="cc1d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc1d6-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1d6-103">建立整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-103">Creates an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc1d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc1d6-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String>
 [-SchemaFilePath <String>] [-SchemaDefinition <String>] [-SchemaType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc1d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="cc1d6-105">DESCRIPTION</span></span>
<span data-ttu-id="cc1d6-106">**新的-AzureRmIntegrationAccountSchema** Cmdlet 會建立整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-106">The **New-AzureRmIntegrationAccountSchema** cmdlet creates an integration account schema.</span></span>
<span data-ttu-id="cc1d6-107">這個 Cmdlet 會傳回代表整合帳戶架構的物件。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-107">This cmdlet returns an object that represents the integration account schema.</span></span>
<span data-ttu-id="cc1d6-108">指定整合帳戶名稱、資源組名稱、架構名稱和架構定義。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-108">Specify the integration account name, resource group name, schema name, and schema definition.</span></span>

<span data-ttu-id="cc1d6-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="cc1d6-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cc1d6-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cc1d6-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cc1d6-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cc1d6-114">示例</span><span class="sxs-lookup"><span data-stu-id="cc1d6-114">EXAMPLES</span></span>

### <span data-ttu-id="cc1d6-115">範例1：建立整合帳戶架構</span><span class="sxs-lookup"><span data-stu-id="cc1d6-115">Example 1: Create the integration account schema</span></span>
```
PS C:\>New-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema1" -SchemaFilePath "c:\temp\schema1"
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/schemas/IntegrationAccountSchema1
Name        : IntegrationAccountSchema1
Type        : Microsoft.Logic/integrationAccounts/schemas
CreatedTime : 3/26/2016 7:21:10 PM
ChangedTime : 3/26/2016 7:21:10 PM
SchemaType  : Xml
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/3839E_XML_INTEGRATIONACCOUNTSCHEMA2-5A6650B914454A2CAB16
              B4A8D3F9840D?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 7901
```

<span data-ttu-id="cc1d6-116">這個命令會在指定的資源群組中建立名為 IntegrationAccountSchema1 的整合帳戶架構。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-116">This command creates the integration account schema named IntegrationAccountSchema1 in the specified resource group.</span></span>

## <span data-ttu-id="cc1d6-117">參數</span><span class="sxs-lookup"><span data-stu-id="cc1d6-117">PARAMETERS</span></span>

### <span data-ttu-id="cc1d6-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="cc1d6-118">-ContentType</span></span>
<span data-ttu-id="cc1d6-119">指定整合帳戶架構的內容類型。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-119">Specifies a content type for the integration account schema.</span></span>
<span data-ttu-id="cc1d6-120">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="cc1d6-121">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="cc1d6-121">-Metadata</span></span>
<span data-ttu-id="cc1d6-122">指定架構的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-122">Specifies a metadata object for the schema.</span></span>

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

### <span data-ttu-id="cc1d6-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc1d6-123">-Name</span></span>
<span data-ttu-id="cc1d6-124">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cc1d6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1d6-125">-ResourceGroupName</span></span>
<span data-ttu-id="cc1d6-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cc1d6-127">-SchemaDefinition</span><span class="sxs-lookup"><span data-stu-id="cc1d6-127">-SchemaDefinition</span></span>
<span data-ttu-id="cc1d6-128">指定整合帳戶架構的定義物件。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-128">Specifies a definition object for integration account schema.</span></span>
<span data-ttu-id="cc1d6-129">請指定此參數或 *SchemaFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-129">Specify either this parameter or the *SchemaFilePath* parameter.</span></span>

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

### <span data-ttu-id="cc1d6-130">-SchemaFilePath</span><span class="sxs-lookup"><span data-stu-id="cc1d6-130">-SchemaFilePath</span></span>
<span data-ttu-id="cc1d6-131">指定整合帳戶架構之定義的檔路徑。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-131">Specifies the file path of a definition for the integration account schema.</span></span>
<span data-ttu-id="cc1d6-132">請指定此參數或 *SchemaDefinition* 參數。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-132">Specify either this parameter or the *SchemaDefinition* parameter.</span></span>

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

### <span data-ttu-id="cc1d6-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="cc1d6-133">-SchemaName</span></span>
<span data-ttu-id="cc1d6-134">指定整合帳戶架構的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-134">Specifies a name for the integration account schema.</span></span>

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

### <span data-ttu-id="cc1d6-135">-SchemaType</span><span class="sxs-lookup"><span data-stu-id="cc1d6-135">-SchemaType</span></span>
<span data-ttu-id="cc1d6-136">指定整合帳戶架構的類型。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-136">Specifies the type for the integration account schema.</span></span>
<span data-ttu-id="cc1d6-137">此參數支援 Xml 作為類型。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-137">This parameter supports Xml as the type.</span></span>

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

### <span data-ttu-id="cc1d6-138">-確認</span><span class="sxs-lookup"><span data-stu-id="cc1d6-138">-Confirm</span></span>
<span data-ttu-id="cc1d6-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc1d6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc1d6-140">-WhatIf</span></span>
<span data-ttu-id="cc1d6-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc1d6-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc1d6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1d6-143">-DefaultProfile</span></span>
<span data-ttu-id="cc1d6-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc1d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1d6-145">CommonParameters</span></span>
<span data-ttu-id="cc1d6-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1d6-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1d6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="cc1d6-148">INPUTS</span></span>

## <span data-ttu-id="cc1d6-149">輸出</span><span class="sxs-lookup"><span data-stu-id="cc1d6-149">OUTPUTS</span></span>

### <span data-ttu-id="cc1d6-150">IntegrationAccountSchema 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="cc1d6-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountSchema</span></span>

## <span data-ttu-id="cc1d6-151">筆記</span><span class="sxs-lookup"><span data-stu-id="cc1d6-151">NOTES</span></span>

## <span data-ttu-id="cc1d6-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc1d6-152">RELATED LINKS</span></span>

[<span data-ttu-id="cc1d6-153">AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cc1d6-153">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="cc1d6-154">移除-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cc1d6-154">Remove-AzureRmIntegrationAccountSchema</span></span>](./Remove-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="cc1d6-155">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="cc1d6-155">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


