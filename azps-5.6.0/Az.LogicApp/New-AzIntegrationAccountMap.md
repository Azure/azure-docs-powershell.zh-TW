---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: DF71430C-F33F-409B-A550-CC7285252E91
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountMap.md
ms.openlocfilehash: 7ce86f893cbead5b2c5ac7a57af44eeb7f92f9ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903594"
---
# <span data-ttu-id="45c22-101">New-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45c22-101">New-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="45c22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="45c22-102">SYNOPSIS</span></span>
<span data-ttu-id="45c22-103">建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="45c22-103">Creates an integration account map.</span></span>

## <span data-ttu-id="45c22-104">語法</span><span class="sxs-lookup"><span data-stu-id="45c22-104">SYNTAX</span></span>

```
New-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c22-105">描述</span><span class="sxs-lookup"><span data-stu-id="45c22-105">DESCRIPTION</span></span>
<span data-ttu-id="45c22-106">**New-AzCountAccountMap** Cmdlet 會建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="45c22-106">The **New-AzIntegrationAccountMap** cmdlet creates an integration account map.</span></span>
<span data-ttu-id="45c22-107">此 Cmdlet 會返回代表整合帳戶地圖的物件。</span><span class="sxs-lookup"><span data-stu-id="45c22-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="45c22-108">指定整合帳戶名稱、資源組名、地圖名稱和地圖定義。</span><span class="sxs-lookup"><span data-stu-id="45c22-108">Specifying the integration account name, resource group name, map name, and map definition.</span></span>
<span data-ttu-id="45c22-109">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="45c22-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="45c22-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="45c22-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="45c22-111">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="45c22-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="45c22-112">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="45c22-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="45c22-113">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="45c22-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="45c22-114">例子</span><span class="sxs-lookup"><span data-stu-id="45c22-114">EXAMPLES</span></span>

### <span data-ttu-id="45c22-115">範例 1：建立整合帳戶地圖</span><span class="sxs-lookup"><span data-stu-id="45c22-115">Example 1: Create an integration account map</span></span>
```powershell
PS C:\>New-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/maps/IntegrationAccountMap47
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

<span data-ttu-id="45c22-116">此命令會建立指定資源群組中的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="45c22-116">This command creates the integration account map in the specified resource group.</span></span>
<span data-ttu-id="45c22-117">命令會指定由上一個命令$MapContent變數中儲存的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="45c22-117">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="45c22-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="45c22-118">Example 2</span></span>

<span data-ttu-id="45c22-119">建立整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="45c22-119">Creates an integration account map.</span></span> <span data-ttu-id="45c22-120"> (自動) </span><span class="sxs-lookup"><span data-stu-id="45c22-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="45c22-121">參數</span><span class="sxs-lookup"><span data-stu-id="45c22-121">PARAMETERS</span></span>

### <span data-ttu-id="45c22-122">-ContentType</span><span class="sxs-lookup"><span data-stu-id="45c22-122">-ContentType</span></span>
<span data-ttu-id="45c22-123">指定整合帳戶地圖的內容類型。</span><span class="sxs-lookup"><span data-stu-id="45c22-123">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="45c22-124">此 Cmdlet 支援應用程式/xml 做為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="45c22-124">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="45c22-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c22-125">-DefaultProfile</span></span>
<span data-ttu-id="45c22-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="45c22-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45c22-127">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="45c22-127">-MapDefinition</span></span>
<span data-ttu-id="45c22-128">指定整合帳戶地圖的定義物件。</span><span class="sxs-lookup"><span data-stu-id="45c22-128">Specifies a definition object for integration account map.</span></span>
<span data-ttu-id="45c22-129">指定此參數或 *MapFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="45c22-129">Specify either this parameter or the *MapFilePath* parameter.</span></span>

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

### <span data-ttu-id="45c22-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="45c22-130">-MapFilePath</span></span>
<span data-ttu-id="45c22-131">指定整合帳戶地圖定義之檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="45c22-131">Specifies the file path of a definition for the integration account map.</span></span> <span data-ttu-id="45c22-132">指定此參數或 *MapDefinition* 參數。</span><span class="sxs-lookup"><span data-stu-id="45c22-132">Specify either this parameter or the *MapDefinition* parameter.</span></span>

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

### <span data-ttu-id="45c22-133">-MapName</span><span class="sxs-lookup"><span data-stu-id="45c22-133">-MapName</span></span>
<span data-ttu-id="45c22-134">指定整合帳戶地圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="45c22-134">Specifies a name for the integration account map.</span></span>

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

### <span data-ttu-id="45c22-135">-MapType</span><span class="sxs-lookup"><span data-stu-id="45c22-135">-MapType</span></span>
<span data-ttu-id="45c22-136">指定整合帳戶地圖的類型。</span><span class="sxs-lookup"><span data-stu-id="45c22-136">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="45c22-137">此 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="45c22-137">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Xslt, Xslt20, Xslt30, Liquid

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c22-138">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="45c22-138">-Metadata</span></span>
<span data-ttu-id="45c22-139">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="45c22-139">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="45c22-140">-名稱</span><span class="sxs-lookup"><span data-stu-id="45c22-140">-Name</span></span>
<span data-ttu-id="45c22-141">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="45c22-141">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="45c22-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c22-142">-ResourceGroupName</span></span>
<span data-ttu-id="45c22-143">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="45c22-143">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="45c22-144">-確認</span><span class="sxs-lookup"><span data-stu-id="45c22-144">-Confirm</span></span>
<span data-ttu-id="45c22-145">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="45c22-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c22-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c22-146">-WhatIf</span></span>
<span data-ttu-id="45c22-147">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="45c22-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c22-148">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45c22-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c22-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c22-149">CommonParameters</span></span>
<span data-ttu-id="45c22-150">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="45c22-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c22-151">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="45c22-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c22-152">輸入</span><span class="sxs-lookup"><span data-stu-id="45c22-152">INPUTS</span></span>

### <span data-ttu-id="45c22-153">System.String</span><span class="sxs-lookup"><span data-stu-id="45c22-153">System.String</span></span>

## <span data-ttu-id="45c22-154">輸出</span><span class="sxs-lookup"><span data-stu-id="45c22-154">OUTPUTS</span></span>

### <span data-ttu-id="45c22-155">Microsoft.Azure.management.Logic.models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="45c22-155">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="45c22-156">筆記</span><span class="sxs-lookup"><span data-stu-id="45c22-156">NOTES</span></span>

## <span data-ttu-id="45c22-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="45c22-157">RELATED LINKS</span></span>

[<span data-ttu-id="45c22-158">Get-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="45c22-158">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="45c22-159">Remove-Az有AccountMap</span><span class="sxs-lookup"><span data-stu-id="45c22-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)

[<span data-ttu-id="45c22-160">Set-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="45c22-160">Set-AzIntegrationAccountMap</span></span>](./Set-AzIntegrationAccountMap.md)


