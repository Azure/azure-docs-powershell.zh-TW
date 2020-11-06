---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 2f6df9b28db7ad86a3c779a166df34c48d779621
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457579"
---
# <span data-ttu-id="2a98f-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2a98f-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="2a98f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a98f-102">SYNOPSIS</span></span>
<span data-ttu-id="2a98f-103">建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="2a98f-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a98f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a98f-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a98f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a98f-105">DESCRIPTION</span></span>
<span data-ttu-id="2a98f-106">**新的-AzureRmIntegrationAccountMap** Cmdlet 會建立整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="2a98f-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="2a98f-107">這個 Cmdlet 會傳回代表整合帳戶對應的物件。</span><span class="sxs-lookup"><span data-stu-id="2a98f-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="2a98f-108">指定整合帳戶名稱、資源組名稱、對應名稱和地圖定義。</span><span class="sxs-lookup"><span data-stu-id="2a98f-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>

<span data-ttu-id="2a98f-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="2a98f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="2a98f-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="2a98f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2a98f-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="2a98f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2a98f-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="2a98f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2a98f-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="2a98f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2a98f-114">示例</span><span class="sxs-lookup"><span data-stu-id="2a98f-114">EXAMPLES</span></span>

### <span data-ttu-id="2a98f-115">範例1：建立整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="2a98f-115">Example 1: Create an integration account map</span></span>
```
PS C:\>New-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/maps/IntegrationAccountMap47
Name        : IntegrationAccountMap47
Type        : Microsoft.Logic/integrationAccounts/maps
CreatedTime : 3/26/2016 7:12:22 PM
ChangedTime : 3/26/2016 7:12:22 PM
MapType     : Xslt
ContentLink : https://<baseurl>/integrationaccounts68a13b6b49f14995ba7c5f3aedcbd7ad/99D1E_XSLT_INTEGRATIONACCOUNTMAP47-9C97D973088B4256A1893B
              BCB1F85246?sv=2014-02-14&sr=b&sig=<value>
ContentSize : 3056
Metadata    :
```

<span data-ttu-id="2a98f-116">這個命令會在指定的資源群組中建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="2a98f-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="2a98f-117">命令會指定由前一個命令儲存在 $MapContent 變數中的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="2a98f-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="2a98f-118">參數</span><span class="sxs-lookup"><span data-stu-id="2a98f-118">PARAMETERS</span></span>

### <span data-ttu-id="2a98f-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="2a98f-119">-ContentType</span></span>
<span data-ttu-id="2a98f-120">指定整合帳戶對應的內容類型。</span><span class="sxs-lookup"><span data-stu-id="2a98f-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="2a98f-121">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="2a98f-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="2a98f-122">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="2a98f-122">-MapDefinition</span></span>
<span data-ttu-id="2a98f-123">指定整合帳戶對應的定義物件。</span><span class="sxs-lookup"><span data-stu-id="2a98f-123">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="2a98f-124">請指定此參數或 *MapFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="2a98f-124">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="2a98f-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="2a98f-125">-MapFilePath</span></span>
<span data-ttu-id="2a98f-126">指定整合帳戶對應的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="2a98f-126">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="2a98f-127">請指定此參數或 *MapDefinition* 參數。</span><span class="sxs-lookup"><span data-stu-id="2a98f-127">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="2a98f-128">-MapName</span><span class="sxs-lookup"><span data-stu-id="2a98f-128">-MapName</span></span>
<span data-ttu-id="2a98f-129">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a98f-129">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="2a98f-130">-MapType</span><span class="sxs-lookup"><span data-stu-id="2a98f-130">-MapType</span></span>
<span data-ttu-id="2a98f-131">指定整合帳戶對應的類型。</span><span class="sxs-lookup"><span data-stu-id="2a98f-131">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="2a98f-132">這個 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="2a98f-132">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a98f-133">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2a98f-133">-Metadata</span></span>
<span data-ttu-id="2a98f-134">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="2a98f-134">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="2a98f-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a98f-135">-Name</span></span>
<span data-ttu-id="2a98f-136">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a98f-136">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="2a98f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a98f-137">-ResourceGroupName</span></span>
<span data-ttu-id="2a98f-138">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a98f-138">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2a98f-139">-確認</span><span class="sxs-lookup"><span data-stu-id="2a98f-139">-Confirm</span></span>
<span data-ttu-id="2a98f-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2a98f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a98f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a98f-141">-WhatIf</span></span>
<span data-ttu-id="2a98f-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2a98f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a98f-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a98f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a98f-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a98f-144">-DefaultProfile</span></span>
<span data-ttu-id="2a98f-145">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a98f-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a98f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a98f-146">CommonParameters</span></span>
<span data-ttu-id="2a98f-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a98f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a98f-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a98f-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a98f-149">輸入</span><span class="sxs-lookup"><span data-stu-id="2a98f-149">INPUTS</span></span>

## <span data-ttu-id="2a98f-150">輸出</span><span class="sxs-lookup"><span data-stu-id="2a98f-150">OUTPUTS</span></span>

### <span data-ttu-id="2a98f-151">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="2a98f-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="2a98f-152">筆記</span><span class="sxs-lookup"><span data-stu-id="2a98f-152">NOTES</span></span>

## <span data-ttu-id="2a98f-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a98f-153">RELATED LINKS</span></span>

[<span data-ttu-id="2a98f-154">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2a98f-154">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="2a98f-155">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2a98f-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="2a98f-156">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="2a98f-156">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


