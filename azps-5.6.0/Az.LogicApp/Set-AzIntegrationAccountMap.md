---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: f963a89e6220e8154c2ba958adca318036c53474
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907106"
---
# <span data-ttu-id="b1ffd-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b1ffd-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="b1ffd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="b1ffd-103">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="b1ffd-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1ffd-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1ffd-105">描述</span><span class="sxs-lookup"><span data-stu-id="b1ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="b1ffd-106">**Set-Az一AccountMap** Cmdlet 會修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="b1ffd-107">此 Cmdlet 會返回代表整合帳戶地圖的物件。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="b1ffd-108">指定整合帳戶名稱、資源組名和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="b1ffd-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b1ffd-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b1ffd-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b1ffd-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b1ffd-113">例子</span><span class="sxs-lookup"><span data-stu-id="b1ffd-113">EXAMPLES</span></span>

### <span data-ttu-id="b1ffd-114">範例 1：修改整合帳戶地圖</span><span class="sxs-lookup"><span data-stu-id="b1ffd-114">Example 1: Modify an integration account map</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="b1ffd-115">此命令會修改指定資源群組中的整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="b1ffd-116">命令會指定由上一個命令$MapContent變數中儲存的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="b1ffd-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="b1ffd-117">Example 2</span></span>

<span data-ttu-id="b1ffd-118">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-118">Modifies an integration account map.</span></span> <span data-ttu-id="b1ffd-119"> (自動) </span><span class="sxs-lookup"><span data-stu-id="b1ffd-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b1ffd-120">參數</span><span class="sxs-lookup"><span data-stu-id="b1ffd-120">PARAMETERS</span></span>

### <span data-ttu-id="b1ffd-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="b1ffd-121">-ContentType</span></span>
<span data-ttu-id="b1ffd-122">指定整合帳戶地圖的內容類型。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="b1ffd-123">此 Cmdlet 支援應用程式/xml 做為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="b1ffd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1ffd-124">-DefaultProfile</span></span>
<span data-ttu-id="b1ffd-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b1ffd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1ffd-126">-強制</span><span class="sxs-lookup"><span data-stu-id="b1ffd-126">-Force</span></span>
<span data-ttu-id="b1ffd-127">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1ffd-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="b1ffd-128">-MapDefinition</span></span>
<span data-ttu-id="b1ffd-129">指定整合帳戶地圖的定義物件。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="b1ffd-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="b1ffd-130">-MapFilePath</span></span>
<span data-ttu-id="b1ffd-131">指定整合帳戶地圖定義之檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="b1ffd-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="b1ffd-132">-MapName</span></span>
<span data-ttu-id="b1ffd-133">指定整合帳戶地圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="b1ffd-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="b1ffd-134">-MapType</span></span>
<span data-ttu-id="b1ffd-135">指定整合帳戶地圖的類型。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="b1ffd-136">此 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="b1ffd-137">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="b1ffd-137">-Metadata</span></span>
<span data-ttu-id="b1ffd-138">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="b1ffd-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="b1ffd-139">-Name</span></span>
<span data-ttu-id="b1ffd-140">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b1ffd-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1ffd-141">-ResourceGroupName</span></span>
<span data-ttu-id="b1ffd-142">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b1ffd-143">-確認</span><span class="sxs-lookup"><span data-stu-id="b1ffd-143">-Confirm</span></span>
<span data-ttu-id="b1ffd-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1ffd-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1ffd-145">-WhatIf</span></span>
<span data-ttu-id="b1ffd-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1ffd-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1ffd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1ffd-148">CommonParameters</span></span>
<span data-ttu-id="b1ffd-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1ffd-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b1ffd-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1ffd-151">輸入</span><span class="sxs-lookup"><span data-stu-id="b1ffd-151">INPUTS</span></span>

### <span data-ttu-id="b1ffd-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b1ffd-152">System.String</span></span>

## <span data-ttu-id="b1ffd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="b1ffd-153">OUTPUTS</span></span>

### <span data-ttu-id="b1ffd-154">Microsoft.Azure.management.Logic.models.IntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="b1ffd-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="b1ffd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="b1ffd-155">NOTES</span></span>

## <span data-ttu-id="b1ffd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1ffd-156">RELATED LINKS</span></span>

[<span data-ttu-id="b1ffd-157">Get-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="b1ffd-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="b1ffd-158">New-AzCountAccountMap</span><span class="sxs-lookup"><span data-stu-id="b1ffd-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="b1ffd-159">Remove-Az有AccountMap</span><span class="sxs-lookup"><span data-stu-id="b1ffd-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


