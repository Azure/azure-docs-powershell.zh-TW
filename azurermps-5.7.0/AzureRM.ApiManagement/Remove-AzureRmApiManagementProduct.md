---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444816"
---
# <span data-ttu-id="3297a-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3297a-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="3297a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3297a-102">SYNOPSIS</span></span>
<span data-ttu-id="3297a-103">移除現有的 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="3297a-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3297a-104">句法</span><span class="sxs-lookup"><span data-stu-id="3297a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3297a-105">說明</span><span class="sxs-lookup"><span data-stu-id="3297a-105">DESCRIPTION</span></span>
<span data-ttu-id="3297a-106">AzureRmApiManagementProduct Cmdlet 會移除現有 **的** API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="3297a-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="3297a-107">示例</span><span class="sxs-lookup"><span data-stu-id="3297a-107">EXAMPLES</span></span>

### <span data-ttu-id="3297a-108">範例1：移除現有產品及所有訂閱</span><span class="sxs-lookup"><span data-stu-id="3297a-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="3297a-109">這個命令會移除現有的產品和所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="3297a-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="3297a-110">參數</span><span class="sxs-lookup"><span data-stu-id="3297a-110">PARAMETERS</span></span>

### <span data-ttu-id="3297a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="3297a-111">-Context</span></span>
<span data-ttu-id="3297a-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="3297a-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3297a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3297a-113">-DefaultProfile</span></span>
<span data-ttu-id="3297a-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3297a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3297a-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="3297a-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="3297a-116">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="3297a-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="3297a-117">如果您未設定此參數，且訂閱存在，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="3297a-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3297a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3297a-118">-PassThru</span></span>
<span data-ttu-id="3297a-119">指出這個 Cmdlet 會傳回 $True 的值（如果它成功的話），或是一個 $False 值（如果它失敗的話）。</span><span class="sxs-lookup"><span data-stu-id="3297a-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3297a-120">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="3297a-120">-ProductId</span></span>
<span data-ttu-id="3297a-121">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3297a-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="3297a-122">-確認</span><span class="sxs-lookup"><span data-stu-id="3297a-122">-Confirm</span></span>
<span data-ttu-id="3297a-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3297a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3297a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3297a-124">-WhatIf</span></span>
<span data-ttu-id="3297a-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3297a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3297a-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3297a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3297a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3297a-127">CommonParameters</span></span>
<span data-ttu-id="3297a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3297a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3297a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3297a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3297a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="3297a-130">INPUTS</span></span>

### <span data-ttu-id="3297a-131">所有</span><span class="sxs-lookup"><span data-stu-id="3297a-131">None</span></span>
<span data-ttu-id="3297a-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3297a-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3297a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="3297a-133">OUTPUTS</span></span>

### <span data-ttu-id="3297a-134">bool</span><span class="sxs-lookup"><span data-stu-id="3297a-134">bool</span></span>

## <span data-ttu-id="3297a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="3297a-135">NOTES</span></span>

## <span data-ttu-id="3297a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="3297a-136">RELATED LINKS</span></span>

[<span data-ttu-id="3297a-137">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3297a-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="3297a-138">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3297a-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="3297a-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="3297a-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


