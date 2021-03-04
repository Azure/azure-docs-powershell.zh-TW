---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908678"
---
# <span data-ttu-id="01137-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="01137-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="01137-102">簡介</span><span class="sxs-lookup"><span data-stu-id="01137-102">SYNOPSIS</span></span>
<span data-ttu-id="01137-103">移除現有的 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="01137-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="01137-104">語法</span><span class="sxs-lookup"><span data-stu-id="01137-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01137-105">描述</span><span class="sxs-lookup"><span data-stu-id="01137-105">DESCRIPTION</span></span>
<span data-ttu-id="01137-106">**Remove-AzApiManagementProduct** Cmdlet 會移除現有的 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="01137-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="01137-107">例子</span><span class="sxs-lookup"><span data-stu-id="01137-107">EXAMPLES</span></span>

### <span data-ttu-id="01137-108">範例 1：移除現有產品及所有訂閱</span><span class="sxs-lookup"><span data-stu-id="01137-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="01137-109">此命令會移除現有的產品及所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="01137-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="01137-110">參數</span><span class="sxs-lookup"><span data-stu-id="01137-110">PARAMETERS</span></span>

### <span data-ttu-id="01137-111">-內容</span><span class="sxs-lookup"><span data-stu-id="01137-111">-Context</span></span>
<span data-ttu-id="01137-112">指定 **PsApiManagementCoNtext 物件的** 實例。</span><span class="sxs-lookup"><span data-stu-id="01137-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01137-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01137-113">-DefaultProfile</span></span>
<span data-ttu-id="01137-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="01137-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01137-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="01137-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="01137-116">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="01137-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="01137-117">如果您未設定此參數，且訂閱存在，系統即會引發例外。</span><span class="sxs-lookup"><span data-stu-id="01137-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="01137-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01137-118">-PassThru</span></span>
<span data-ttu-id="01137-119">表示此 Cmdlet 會$True成功時，或如果失敗時$False值。</span><span class="sxs-lookup"><span data-stu-id="01137-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="01137-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="01137-120">-ProductId</span></span>
<span data-ttu-id="01137-121">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="01137-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="01137-122">-確認</span><span class="sxs-lookup"><span data-stu-id="01137-122">-Confirm</span></span>
<span data-ttu-id="01137-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="01137-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01137-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01137-124">-WhatIf</span></span>
<span data-ttu-id="01137-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01137-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01137-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01137-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01137-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01137-127">CommonParameters</span></span>
<span data-ttu-id="01137-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="01137-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01137-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01137-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01137-130">輸入</span><span class="sxs-lookup"><span data-stu-id="01137-130">INPUTS</span></span>

### <span data-ttu-id="01137-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="01137-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01137-132">System.String</span><span class="sxs-lookup"><span data-stu-id="01137-132">System.String</span></span>

### <span data-ttu-id="01137-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="01137-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="01137-134">輸出</span><span class="sxs-lookup"><span data-stu-id="01137-134">OUTPUTS</span></span>

### <span data-ttu-id="01137-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01137-135">System.Boolean</span></span>

## <span data-ttu-id="01137-136">筆記</span><span class="sxs-lookup"><span data-stu-id="01137-136">NOTES</span></span>

## <span data-ttu-id="01137-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="01137-137">RELATED LINKS</span></span>

[<span data-ttu-id="01137-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="01137-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="01137-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="01137-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="01137-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="01137-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


