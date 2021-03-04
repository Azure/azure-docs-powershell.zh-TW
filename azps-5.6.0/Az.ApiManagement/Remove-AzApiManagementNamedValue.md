---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: 3101f58720130a6e5f7c91fb4489d96915d8c4e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903378"
---
# <span data-ttu-id="b65cf-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="b65cf-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="b65cf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b65cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b65cf-103">移除 API 管理命名值。</span><span class="sxs-lookup"><span data-stu-id="b65cf-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="b65cf-104">語法</span><span class="sxs-lookup"><span data-stu-id="b65cf-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b65cf-105">描述</span><span class="sxs-lookup"><span data-stu-id="b65cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b65cf-106">**Remove-AzApiManagementNamedValue** Cmdlet 會移除 Azure API 管理 **具名值**。</span><span class="sxs-lookup"><span data-stu-id="b65cf-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="b65cf-107">例子</span><span class="sxs-lookup"><span data-stu-id="b65cf-107">EXAMPLES</span></span>

### <span data-ttu-id="b65cf-108">範例 1：移除已命名的值</span><span class="sxs-lookup"><span data-stu-id="b65cf-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="b65cf-109">此命令會移除具有 ID 屬性11 的命名值。</span><span class="sxs-lookup"><span data-stu-id="b65cf-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="b65cf-110">參數</span><span class="sxs-lookup"><span data-stu-id="b65cf-110">PARAMETERS</span></span>

### <span data-ttu-id="b65cf-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b65cf-111">-Context</span></span>
<span data-ttu-id="b65cf-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b65cf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b65cf-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b65cf-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b65cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65cf-114">-DefaultProfile</span></span>
<span data-ttu-id="b65cf-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b65cf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65cf-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="b65cf-116">-NamedValueId</span></span>
<span data-ttu-id="b65cf-117">現有命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b65cf-117">Identifier of existing named value.</span></span>
<span data-ttu-id="b65cf-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b65cf-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b65cf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b65cf-119">-PassThru</span></span>
<span data-ttu-id="b65cf-120">如果指定，如果作業成功，會寫入 True。</span><span class="sxs-lookup"><span data-stu-id="b65cf-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b65cf-121">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="b65cf-121">This parameter is optional.</span></span>
<span data-ttu-id="b65cf-122">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="b65cf-122">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65cf-123">-確認</span><span class="sxs-lookup"><span data-stu-id="b65cf-123">-Confirm</span></span>
<span data-ttu-id="b65cf-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b65cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65cf-125">-WhatIf</span></span>
<span data-ttu-id="b65cf-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b65cf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65cf-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b65cf-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b65cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65cf-128">CommonParameters</span></span>
<span data-ttu-id="b65cf-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b65cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65cf-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b65cf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65cf-131">輸入</span><span class="sxs-lookup"><span data-stu-id="b65cf-131">INPUTS</span></span>

### <span data-ttu-id="b65cf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b65cf-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b65cf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b65cf-133">System.String</span></span>

### <span data-ttu-id="b65cf-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b65cf-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b65cf-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b65cf-135">OUTPUTS</span></span>

### <span data-ttu-id="b65cf-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b65cf-136">System.Boolean</span></span>

## <span data-ttu-id="b65cf-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b65cf-137">NOTES</span></span>

## <span data-ttu-id="b65cf-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b65cf-138">RELATED LINKS</span></span>
