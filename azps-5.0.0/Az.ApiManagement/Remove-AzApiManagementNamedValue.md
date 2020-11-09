---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementNamedValue.md
ms.openlocfilehash: c2cf7f46a7f7f73443a9d7d2b06dbfde943b28d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288407"
---
# <span data-ttu-id="0b0c3-101">Remove-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="0b0c3-101">Remove-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="0b0c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="0b0c3-103">移除 API 管理命名值。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-103">Removes an API Management Named Value.</span></span>

## <span data-ttu-id="0b0c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b0c3-104">SYNTAX</span></span>

```
Remove-AzApiManagementNamedValue -Context <PsApiManagementContext> -NamedValueId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b0c3-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b0c3-105">DESCRIPTION</span></span>
<span data-ttu-id="0b0c3-106">**AzApiManagementNamedValue** Cmdlet 會移除 Azure API 管理 **命名值** 。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-106">The **Remove-AzApiManagementNamedValue** cmdlet removes an Azure API Management **Named Value**.</span></span>

## <span data-ttu-id="0b0c3-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b0c3-107">EXAMPLES</span></span>

### <span data-ttu-id="0b0c3-108">範例1：移除命名值</span><span class="sxs-lookup"><span data-stu-id="0b0c3-108">Example 1: Remove the named value</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementNamedValue -Context $apimContext -NamedValueId "Property11" -PassThru
```

<span data-ttu-id="0b0c3-109">這個命令會移除具有識別碼 Property11 的命名值。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-109">This command removes the named value that has the ID Property11.</span></span>

## <span data-ttu-id="0b0c3-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b0c3-110">PARAMETERS</span></span>

### <span data-ttu-id="0b0c3-111">-內容</span><span class="sxs-lookup"><span data-stu-id="0b0c3-111">-Context</span></span>
<span data-ttu-id="0b0c3-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0b0c3-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-113">This parameter is required.</span></span>

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

### <span data-ttu-id="0b0c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b0c3-114">-DefaultProfile</span></span>
<span data-ttu-id="0b0c3-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b0c3-116">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="0b0c3-116">-NamedValueId</span></span>
<span data-ttu-id="0b0c3-117">現有命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-117">Identifier of existing named value.</span></span>
<span data-ttu-id="0b0c3-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0b0c3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0b0c3-119">-PassThru</span></span>
<span data-ttu-id="0b0c3-120">如果已指定，則會在操作成功時寫入 true。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-120">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0b0c3-121">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-121">This parameter is optional.</span></span>
<span data-ttu-id="0b0c3-122">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-122">Default value is false.</span></span>

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

### <span data-ttu-id="0b0c3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="0b0c3-123">-Confirm</span></span>
<span data-ttu-id="0b0c3-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b0c3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b0c3-125">-WhatIf</span></span>
<span data-ttu-id="0b0c3-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b0c3-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b0c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b0c3-128">CommonParameters</span></span>
<span data-ttu-id="0b0c3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b0c3-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b0c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b0c3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0b0c3-131">INPUTS</span></span>

### <span data-ttu-id="0b0c3-132">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="0b0c3-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0b0c3-133">System.object</span><span class="sxs-lookup"><span data-stu-id="0b0c3-133">System.String</span></span>

### <span data-ttu-id="0b0c3-134">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="0b0c3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0b0c3-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0b0c3-135">OUTPUTS</span></span>

### <span data-ttu-id="0b0c3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="0b0c3-136">System.Boolean</span></span>

## <span data-ttu-id="0b0c3-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0b0c3-137">NOTES</span></span>

## <span data-ttu-id="0b0c3-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b0c3-138">RELATED LINKS</span></span>
