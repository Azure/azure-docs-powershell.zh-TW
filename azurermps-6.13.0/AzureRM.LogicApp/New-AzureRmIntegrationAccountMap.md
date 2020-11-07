---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 1b4f46832b08928fe64b080f10331441248065d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626089"
---
# <span data-ttu-id="d84d5-101">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d84d5-101">New-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="d84d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d84d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d84d5-103">建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="d84d5-103">Creates an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d84d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d84d5-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d84d5-105">說明</span><span class="sxs-lookup"><span data-stu-id="d84d5-105">DESCRIPTION</span></span>
<span data-ttu-id="d84d5-106">**新的-AzureRmIntegrationAccountMap** Cmdlet 會建立整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="d84d5-106">The **New-AzureRmIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="d84d5-107">這個 Cmdlet 會傳回代表整合帳戶對應的物件。</span><span class="sxs-lookup"><span data-stu-id="d84d5-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="d84d5-108">指定整合帳戶名稱、資源組名稱、對應名稱和地圖定義。</span><span class="sxs-lookup"><span data-stu-id="d84d5-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="d84d5-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="d84d5-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d84d5-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d84d5-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d84d5-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d84d5-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d84d5-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d84d5-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d84d5-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d84d5-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d84d5-114">示例</span><span class="sxs-lookup"><span data-stu-id="d84d5-114">EXAMPLES</span></span>

### <span data-ttu-id="d84d5-115">範例1：建立整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="d84d5-115">Example 1: Create an integration account map</span></span>
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

<span data-ttu-id="d84d5-116">這個命令會在指定的資源群組中建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="d84d5-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="d84d5-117">命令會指定由前一個命令儲存在 $MapContent 變數中的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="d84d5-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="d84d5-118">參數</span><span class="sxs-lookup"><span data-stu-id="d84d5-118">PARAMETERS</span></span>

### <span data-ttu-id="d84d5-119">-ContentType</span><span class="sxs-lookup"><span data-stu-id="d84d5-119">-ContentType</span></span>
<span data-ttu-id="d84d5-120">指定整合帳戶對應的內容類型。</span><span class="sxs-lookup"><span data-stu-id="d84d5-120">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="d84d5-121">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="d84d5-121">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="d84d5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84d5-122">-DefaultProfile</span></span>
<span data-ttu-id="d84d5-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d84d5-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d84d5-124">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="d84d5-124">-MapDefinition</span></span>
<span data-ttu-id="d84d5-125">指定整合帳戶對應的定義物件。</span><span class="sxs-lookup"><span data-stu-id="d84d5-125">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="d84d5-126">請指定此參數或 *MapFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="d84d5-126">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="d84d5-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="d84d5-127">-MapFilePath</span></span>
<span data-ttu-id="d84d5-128">指定整合帳戶對應的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d84d5-128">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="d84d5-129">請指定此參數或 *MapDefinition* 參數。</span><span class="sxs-lookup"><span data-stu-id="d84d5-129">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="d84d5-130">-MapName</span><span class="sxs-lookup"><span data-stu-id="d84d5-130">-MapName</span></span>
<span data-ttu-id="d84d5-131">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="d84d5-131">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="d84d5-132">-MapType</span><span class="sxs-lookup"><span data-stu-id="d84d5-132">-MapType</span></span>
<span data-ttu-id="d84d5-133">指定整合帳戶對應的類型。</span><span class="sxs-lookup"><span data-stu-id="d84d5-133">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="d84d5-134">這個 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="d84d5-134">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="d84d5-135">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="d84d5-135">-Metadata</span></span>
<span data-ttu-id="d84d5-136">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="d84d5-136">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="d84d5-137">-名稱</span><span class="sxs-lookup"><span data-stu-id="d84d5-137">-Name</span></span>
<span data-ttu-id="d84d5-138">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d84d5-138">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="d84d5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d84d5-139">-ResourceGroupName</span></span>
<span data-ttu-id="d84d5-140">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d84d5-140">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="d84d5-141">-確認</span><span class="sxs-lookup"><span data-stu-id="d84d5-141">-Confirm</span></span>
<span data-ttu-id="d84d5-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d84d5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d84d5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d84d5-143">-WhatIf</span></span>
<span data-ttu-id="d84d5-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d84d5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d84d5-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d84d5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d84d5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84d5-146">CommonParameters</span></span>
<span data-ttu-id="d84d5-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d84d5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84d5-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d84d5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84d5-149">輸入</span><span class="sxs-lookup"><span data-stu-id="d84d5-149">INPUTS</span></span>

### <span data-ttu-id="d84d5-150">System.object</span><span class="sxs-lookup"><span data-stu-id="d84d5-150">System.String</span></span>

## <span data-ttu-id="d84d5-151">輸出</span><span class="sxs-lookup"><span data-stu-id="d84d5-151">OUTPUTS</span></span>

### <span data-ttu-id="d84d5-152">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="d84d5-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="d84d5-153">筆記</span><span class="sxs-lookup"><span data-stu-id="d84d5-153">NOTES</span></span>

## <span data-ttu-id="d84d5-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="d84d5-154">RELATED LINKS</span></span>

[<span data-ttu-id="d84d5-155">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d84d5-155">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="d84d5-156">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d84d5-156">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="d84d5-157">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="d84d5-157">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


