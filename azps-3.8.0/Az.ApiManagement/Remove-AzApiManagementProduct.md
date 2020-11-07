---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958083"
---
# <span data-ttu-id="60f67-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="60f67-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="60f67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60f67-102">SYNOPSIS</span></span>
<span data-ttu-id="60f67-103">移除現有的 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="60f67-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="60f67-104">句法</span><span class="sxs-lookup"><span data-stu-id="60f67-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60f67-105">說明</span><span class="sxs-lookup"><span data-stu-id="60f67-105">DESCRIPTION</span></span>
<span data-ttu-id="60f67-106">AzApiManagementProduct Cmdlet 會移除現有 **的** API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="60f67-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="60f67-107">示例</span><span class="sxs-lookup"><span data-stu-id="60f67-107">EXAMPLES</span></span>

### <span data-ttu-id="60f67-108">範例1：移除現有產品及所有訂閱</span><span class="sxs-lookup"><span data-stu-id="60f67-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="60f67-109">這個命令會移除現有的產品和所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="60f67-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="60f67-110">參數</span><span class="sxs-lookup"><span data-stu-id="60f67-110">PARAMETERS</span></span>

### <span data-ttu-id="60f67-111">-內容</span><span class="sxs-lookup"><span data-stu-id="60f67-111">-Context</span></span>
<span data-ttu-id="60f67-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="60f67-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="60f67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60f67-113">-DefaultProfile</span></span>
<span data-ttu-id="60f67-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60f67-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60f67-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="60f67-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="60f67-116">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="60f67-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="60f67-117">如果您未設定此參數，且訂閱存在，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="60f67-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="60f67-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60f67-118">-PassThru</span></span>
<span data-ttu-id="60f67-119">指出這個 Cmdlet 會傳回 $True 的值（如果它成功的話），或是一個 $False 值（如果它失敗的話）。</span><span class="sxs-lookup"><span data-stu-id="60f67-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="60f67-120">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="60f67-120">-ProductId</span></span>
<span data-ttu-id="60f67-121">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="60f67-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="60f67-122">-確認</span><span class="sxs-lookup"><span data-stu-id="60f67-122">-Confirm</span></span>
<span data-ttu-id="60f67-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60f67-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60f67-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60f67-124">-WhatIf</span></span>
<span data-ttu-id="60f67-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60f67-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60f67-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60f67-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60f67-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60f67-127">CommonParameters</span></span>
<span data-ttu-id="60f67-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60f67-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60f67-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="60f67-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60f67-130">輸入</span><span class="sxs-lookup"><span data-stu-id="60f67-130">INPUTS</span></span>

### <span data-ttu-id="60f67-131">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="60f67-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="60f67-132">System.object</span><span class="sxs-lookup"><span data-stu-id="60f67-132">System.String</span></span>

### <span data-ttu-id="60f67-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="60f67-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60f67-134">輸出</span><span class="sxs-lookup"><span data-stu-id="60f67-134">OUTPUTS</span></span>

### <span data-ttu-id="60f67-135">System.object</span><span class="sxs-lookup"><span data-stu-id="60f67-135">System.Boolean</span></span>

## <span data-ttu-id="60f67-136">筆記</span><span class="sxs-lookup"><span data-stu-id="60f67-136">NOTES</span></span>

## <span data-ttu-id="60f67-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="60f67-137">RELATED LINKS</span></span>

[<span data-ttu-id="60f67-138">AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="60f67-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="60f67-139">新-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="60f67-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="60f67-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="60f67-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


