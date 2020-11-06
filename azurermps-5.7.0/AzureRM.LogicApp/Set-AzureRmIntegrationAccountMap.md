---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 04cd6204b93a0ce84f025d6af931c5f5e287c558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450559"
---
# <span data-ttu-id="999b7-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="999b7-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="999b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="999b7-102">SYNOPSIS</span></span>
<span data-ttu-id="999b7-103">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="999b7-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="999b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="999b7-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="999b7-105">說明</span><span class="sxs-lookup"><span data-stu-id="999b7-105">DESCRIPTION</span></span>
<span data-ttu-id="999b7-106">**AzureRmIntegrationAccountMap** Cmdlet 會修改整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="999b7-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="999b7-107">這個 Cmdlet 會傳回代表整合帳戶對應的物件。</span><span class="sxs-lookup"><span data-stu-id="999b7-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="999b7-108">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="999b7-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="999b7-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="999b7-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="999b7-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="999b7-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="999b7-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="999b7-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="999b7-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="999b7-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="999b7-113">示例</span><span class="sxs-lookup"><span data-stu-id="999b7-113">EXAMPLES</span></span>

### <span data-ttu-id="999b7-114">範例1：修改整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="999b7-114">Example 1: Modify an integration account map</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47" -MapDefinition $MapContent
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

<span data-ttu-id="999b7-115">這個命令會修改指定資源群組中的整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="999b7-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="999b7-116">命令會指定由前一個命令儲存在 $MapContent 變數中的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="999b7-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="999b7-117">參數</span><span class="sxs-lookup"><span data-stu-id="999b7-117">PARAMETERS</span></span>

### <span data-ttu-id="999b7-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="999b7-118">-ContentType</span></span>
<span data-ttu-id="999b7-119">指定整合帳戶對應的內容類型。</span><span class="sxs-lookup"><span data-stu-id="999b7-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="999b7-120">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="999b7-120">This cmdlet supports application/xml as a map content type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="999b7-121">-DefaultProfile</span></span>
<span data-ttu-id="999b7-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="999b7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-123">-Force</span><span class="sxs-lookup"><span data-stu-id="999b7-123">-Force</span></span>
<span data-ttu-id="999b7-124">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="999b7-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-125">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="999b7-125">-MapDefinition</span></span>
<span data-ttu-id="999b7-126">指定整合帳戶對應的定義物件。</span><span class="sxs-lookup"><span data-stu-id="999b7-126">Specifies a definition object for integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-127">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="999b7-127">-MapFilePath</span></span>
<span data-ttu-id="999b7-128">指定整合帳戶對應的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="999b7-128">Specifies the file path of a definition for the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-129">-MapName</span><span class="sxs-lookup"><span data-stu-id="999b7-129">-MapName</span></span>
<span data-ttu-id="999b7-130">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="999b7-130">Specifies the name of an integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-131">-MapType</span><span class="sxs-lookup"><span data-stu-id="999b7-131">-MapType</span></span>
<span data-ttu-id="999b7-132">指定整合帳戶對應的類型。</span><span class="sxs-lookup"><span data-stu-id="999b7-132">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="999b7-133">這個 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="999b7-133">This cmdlet supports Xslt as a map type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Xslt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-134">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="999b7-134">-Metadata</span></span>
<span data-ttu-id="999b7-135">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="999b7-135">Specifies a metadata object for the map.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="999b7-136">-Name</span></span>
<span data-ttu-id="999b7-137">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="999b7-137">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="999b7-138">-ResourceGroupName</span></span>
<span data-ttu-id="999b7-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="999b7-139">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-140">-確認</span><span class="sxs-lookup"><span data-stu-id="999b7-140">-Confirm</span></span>
<span data-ttu-id="999b7-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="999b7-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="999b7-142">-WhatIf</span></span>
<span data-ttu-id="999b7-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="999b7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="999b7-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="999b7-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="999b7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="999b7-145">CommonParameters</span></span>
<span data-ttu-id="999b7-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="999b7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="999b7-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="999b7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="999b7-148">輸入</span><span class="sxs-lookup"><span data-stu-id="999b7-148">INPUTS</span></span>

### <span data-ttu-id="999b7-149">所有</span><span class="sxs-lookup"><span data-stu-id="999b7-149">None</span></span>
<span data-ttu-id="999b7-150">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="999b7-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="999b7-151">輸出</span><span class="sxs-lookup"><span data-stu-id="999b7-151">OUTPUTS</span></span>

### <span data-ttu-id="999b7-152">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="999b7-152">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="999b7-153">筆記</span><span class="sxs-lookup"><span data-stu-id="999b7-153">NOTES</span></span>

## <span data-ttu-id="999b7-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="999b7-154">RELATED LINKS</span></span>

[<span data-ttu-id="999b7-155">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="999b7-155">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="999b7-156">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="999b7-156">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="999b7-157">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="999b7-157">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


