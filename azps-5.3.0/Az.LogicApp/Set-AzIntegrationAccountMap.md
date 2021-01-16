---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountMap.md
ms.openlocfilehash: fd077d5648f831c0b7c0562c3d3bcb642bd639b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435329"
---
# <span data-ttu-id="23303-101">Set-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="23303-101">Set-AzIntegrationAccountMap</span></span>

## <span data-ttu-id="23303-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23303-102">SYNOPSIS</span></span>
<span data-ttu-id="23303-103">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="23303-103">Modifies an integration account map.</span></span>

## <span data-ttu-id="23303-104">句法</span><span class="sxs-lookup"><span data-stu-id="23303-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23303-105">說明</span><span class="sxs-lookup"><span data-stu-id="23303-105">DESCRIPTION</span></span>
<span data-ttu-id="23303-106">**AzIntegrationAccountMap** Cmdlet 會修改整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="23303-106">The **Set-AzIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="23303-107">這個 Cmdlet 會傳回代表整合帳戶對應的物件。</span><span class="sxs-lookup"><span data-stu-id="23303-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="23303-108">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="23303-108">Specify the integration account name, resource group name, and map name.</span></span>
<span data-ttu-id="23303-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="23303-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="23303-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="23303-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="23303-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="23303-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="23303-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="23303-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="23303-113">示例</span><span class="sxs-lookup"><span data-stu-id="23303-113">EXAMPLES</span></span>

### <span data-ttu-id="23303-114">範例1：修改整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="23303-114">Example 1: Modify an integration account map</span></span>
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

<span data-ttu-id="23303-115">這個命令會修改指定資源群組中的整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="23303-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="23303-116">命令會指定由前一個命令儲存在 $MapContent 變數中的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="23303-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

### <span data-ttu-id="23303-117">範例2</span><span class="sxs-lookup"><span data-stu-id="23303-117">Example 2</span></span>

<span data-ttu-id="23303-118">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="23303-118">Modifies an integration account map.</span></span> <span data-ttu-id="23303-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="23303-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountMap -MapFilePath <String> -MapName 'IntegrationAccountMap47' -MapType Xslt -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="23303-120">參數</span><span class="sxs-lookup"><span data-stu-id="23303-120">PARAMETERS</span></span>

### <span data-ttu-id="23303-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="23303-121">-ContentType</span></span>
<span data-ttu-id="23303-122">指定整合帳戶對應的內容類型。</span><span class="sxs-lookup"><span data-stu-id="23303-122">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="23303-123">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="23303-123">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="23303-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23303-124">-DefaultProfile</span></span>
<span data-ttu-id="23303-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23303-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23303-126">-Force</span><span class="sxs-lookup"><span data-stu-id="23303-126">-Force</span></span>
<span data-ttu-id="23303-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="23303-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23303-128">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="23303-128">-MapDefinition</span></span>
<span data-ttu-id="23303-129">指定整合帳戶對應的定義物件。</span><span class="sxs-lookup"><span data-stu-id="23303-129">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="23303-130">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="23303-130">-MapFilePath</span></span>
<span data-ttu-id="23303-131">指定整合帳戶對應的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="23303-131">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="23303-132">-MapName</span><span class="sxs-lookup"><span data-stu-id="23303-132">-MapName</span></span>
<span data-ttu-id="23303-133">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="23303-133">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="23303-134">-MapType</span><span class="sxs-lookup"><span data-stu-id="23303-134">-MapType</span></span>
<span data-ttu-id="23303-135">指定整合帳戶對應的類型。</span><span class="sxs-lookup"><span data-stu-id="23303-135">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="23303-136">這個 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="23303-136">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="23303-137">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="23303-137">-Metadata</span></span>
<span data-ttu-id="23303-138">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="23303-138">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="23303-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="23303-139">-Name</span></span>
<span data-ttu-id="23303-140">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="23303-140">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="23303-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23303-141">-ResourceGroupName</span></span>
<span data-ttu-id="23303-142">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23303-142">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="23303-143">-確認</span><span class="sxs-lookup"><span data-stu-id="23303-143">-Confirm</span></span>
<span data-ttu-id="23303-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23303-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23303-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23303-145">-WhatIf</span></span>
<span data-ttu-id="23303-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23303-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23303-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23303-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23303-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23303-148">CommonParameters</span></span>
<span data-ttu-id="23303-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23303-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23303-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23303-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23303-151">輸入</span><span class="sxs-lookup"><span data-stu-id="23303-151">INPUTS</span></span>

### <span data-ttu-id="23303-152">System.object</span><span class="sxs-lookup"><span data-stu-id="23303-152">System.String</span></span>

## <span data-ttu-id="23303-153">輸出</span><span class="sxs-lookup"><span data-stu-id="23303-153">OUTPUTS</span></span>

### <span data-ttu-id="23303-154">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="23303-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="23303-155">筆記</span><span class="sxs-lookup"><span data-stu-id="23303-155">NOTES</span></span>

## <span data-ttu-id="23303-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="23303-156">RELATED LINKS</span></span>

[<span data-ttu-id="23303-157">AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="23303-157">Get-AzIntegrationAccountMap</span></span>](./Get-AzIntegrationAccountMap.md)

[<span data-ttu-id="23303-158">新-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="23303-158">New-AzIntegrationAccountMap</span></span>](./New-AzIntegrationAccountMap.md)

[<span data-ttu-id="23303-159">移除-AzIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="23303-159">Remove-AzIntegrationAccountMap</span></span>](./Remove-AzIntegrationAccountMap.md)


