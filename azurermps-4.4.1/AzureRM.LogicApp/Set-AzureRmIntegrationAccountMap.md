---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7EF87BE5-FB10-4E5D-A12F-7F50EE6DAD57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 3e4a8a68ce6af6a8be30750d0eaf8e5393ac409f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625154"
---
# <span data-ttu-id="17333-101">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17333-101">Set-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="17333-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17333-102">SYNOPSIS</span></span>
<span data-ttu-id="17333-103">修改整合帳戶地圖。</span><span class="sxs-lookup"><span data-stu-id="17333-103">Modifies an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17333-104">句法</span><span class="sxs-lookup"><span data-stu-id="17333-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String>
 [-MapFilePath <String>] [-MapDefinition <String>] [-MapType <String>] [-ContentType <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17333-105">說明</span><span class="sxs-lookup"><span data-stu-id="17333-105">DESCRIPTION</span></span>
<span data-ttu-id="17333-106">**AzureRmIntegrationAccountMap** Cmdlet 會修改整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="17333-106">The **Set-AzureRmIntegrationAccountMap** cmdlet modifies an integration account map.</span></span>
<span data-ttu-id="17333-107">這個 Cmdlet 會傳回代表整合帳戶對應的物件。</span><span class="sxs-lookup"><span data-stu-id="17333-107">This cmdlet returns an object that represents the integration account map.</span></span>
<span data-ttu-id="17333-108">指定整合帳戶名稱、資源群組名稱和地圖名稱。</span><span class="sxs-lookup"><span data-stu-id="17333-108">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="17333-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="17333-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="17333-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="17333-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="17333-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="17333-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="17333-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="17333-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="17333-113">示例</span><span class="sxs-lookup"><span data-stu-id="17333-113">EXAMPLES</span></span>

### <span data-ttu-id="17333-114">範例1：修改整合帳戶對應</span><span class="sxs-lookup"><span data-stu-id="17333-114">Example 1: Modify an integration account map</span></span>
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

<span data-ttu-id="17333-115">這個命令會修改指定資源群組中的整合帳戶對應。</span><span class="sxs-lookup"><span data-stu-id="17333-115">This command modifies the integration account map in the specified resource group.</span></span>
<span data-ttu-id="17333-116">命令會指定由前一個命令儲存在 $MapContent 變數中的地圖定義。</span><span class="sxs-lookup"><span data-stu-id="17333-116">The command specifies a map definition stored in the $MapContent variable by a previous command.</span></span>

## <span data-ttu-id="17333-117">參數</span><span class="sxs-lookup"><span data-stu-id="17333-117">PARAMETERS</span></span>

### <span data-ttu-id="17333-118">-ContentType</span><span class="sxs-lookup"><span data-stu-id="17333-118">-ContentType</span></span>
<span data-ttu-id="17333-119">指定整合帳戶對應的內容類型。</span><span class="sxs-lookup"><span data-stu-id="17333-119">Specifies a content type for the integration account map.</span></span>
<span data-ttu-id="17333-120">這個 Cmdlet 支援 application/xml 作為地圖內容類型。</span><span class="sxs-lookup"><span data-stu-id="17333-120">This cmdlet supports application/xml as a map content type.</span></span>

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

### <span data-ttu-id="17333-121">-Force</span><span class="sxs-lookup"><span data-stu-id="17333-121">-Force</span></span>
<span data-ttu-id="17333-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="17333-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17333-123">-MapDefinition</span><span class="sxs-lookup"><span data-stu-id="17333-123">-MapDefinition</span></span>
<span data-ttu-id="17333-124">指定整合帳戶對應的定義物件。</span><span class="sxs-lookup"><span data-stu-id="17333-124">Specifies a definition object for integration account map.</span></span>

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

### <span data-ttu-id="17333-125">-MapFilePath</span><span class="sxs-lookup"><span data-stu-id="17333-125">-MapFilePath</span></span>
<span data-ttu-id="17333-126">指定整合帳戶對應的定義檔路徑。</span><span class="sxs-lookup"><span data-stu-id="17333-126">Specifies the file path of a definition for the integration account map.</span></span>

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

### <span data-ttu-id="17333-127">-MapName</span><span class="sxs-lookup"><span data-stu-id="17333-127">-MapName</span></span>
<span data-ttu-id="17333-128">指定整合帳戶對應的名稱。</span><span class="sxs-lookup"><span data-stu-id="17333-128">Specifies the name of an integration account map.</span></span>

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

### <span data-ttu-id="17333-129">-MapType</span><span class="sxs-lookup"><span data-stu-id="17333-129">-MapType</span></span>
<span data-ttu-id="17333-130">指定整合帳戶對應的類型。</span><span class="sxs-lookup"><span data-stu-id="17333-130">Specifies the type for the integration account map.</span></span>
<span data-ttu-id="17333-131">這個 Cmdlet 支援 Xslt 做為地圖類型。</span><span class="sxs-lookup"><span data-stu-id="17333-131">This cmdlet supports Xslt as a map type.</span></span>

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

### <span data-ttu-id="17333-132">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="17333-132">-Metadata</span></span>
<span data-ttu-id="17333-133">指定地圖的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="17333-133">Specifies a metadata object for the map.</span></span>

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

### <span data-ttu-id="17333-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="17333-134">-Name</span></span>
<span data-ttu-id="17333-135">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="17333-135">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="17333-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17333-136">-ResourceGroupName</span></span>
<span data-ttu-id="17333-137">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17333-137">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="17333-138">-確認</span><span class="sxs-lookup"><span data-stu-id="17333-138">-Confirm</span></span>
<span data-ttu-id="17333-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17333-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17333-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17333-140">-WhatIf</span></span>
<span data-ttu-id="17333-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17333-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17333-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17333-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17333-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17333-143">-DefaultProfile</span></span>
<span data-ttu-id="17333-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17333-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17333-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17333-145">CommonParameters</span></span>
<span data-ttu-id="17333-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17333-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17333-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17333-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17333-148">輸入</span><span class="sxs-lookup"><span data-stu-id="17333-148">INPUTS</span></span>

## <span data-ttu-id="17333-149">輸出</span><span class="sxs-lookup"><span data-stu-id="17333-149">OUTPUTS</span></span>

### <span data-ttu-id="17333-150">IntegrationAccountMap 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="17333-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountMap</span></span>

## <span data-ttu-id="17333-151">筆記</span><span class="sxs-lookup"><span data-stu-id="17333-151">NOTES</span></span>

## <span data-ttu-id="17333-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="17333-152">RELATED LINKS</span></span>

[<span data-ttu-id="17333-153">AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17333-153">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="17333-154">新-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17333-154">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="17333-155">移除-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="17333-155">Remove-AzureRmIntegrationAccountMap</span></span>](./Remove-AzureRmIntegrationAccountMap.md)


