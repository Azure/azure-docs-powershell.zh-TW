---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445195"
---
# <span data-ttu-id="1bc3a-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1bc3a-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="1bc3a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1bc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc3a-103">移除現有的 API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bc3a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1bc3a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bc3a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1bc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="1bc3a-106">AzureRmApiManagementProduct Cmdlet 會移除現有 **的** API 管理產品。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="1bc3a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1bc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="1bc3a-108">範例1：移除現有產品及所有訂閱</span><span class="sxs-lookup"><span data-stu-id="1bc3a-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="1bc3a-109">這個命令會移除現有的產品和所有訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="1bc3a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1bc3a-110">PARAMETERS</span></span>

### <span data-ttu-id="1bc3a-111">-內容</span><span class="sxs-lookup"><span data-stu-id="1bc3a-111">-Context</span></span>
<span data-ttu-id="1bc3a-112">指定 **PsApiManagementCoNtext** 物件的實例。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bc3a-113">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="1bc3a-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="1bc3a-114">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="1bc3a-115">如果您未設定此參數，且訂閱存在，則會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="1bc3a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bc3a-116">-PassThru</span></span>
<span data-ttu-id="1bc3a-117">指出這個 Cmdlet 會傳回 $True 的值（如果它成功的話），或是一個 $False 值（如果它失敗的話）。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="1bc3a-118">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="1bc3a-118">-ProductId</span></span>
<span data-ttu-id="1bc3a-119">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="1bc3a-120">-確認</span><span class="sxs-lookup"><span data-stu-id="1bc3a-120">-Confirm</span></span>
<span data-ttu-id="1bc3a-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bc3a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc3a-122">-WhatIf</span></span>
<span data-ttu-id="1bc3a-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bc3a-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bc3a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bc3a-125">-DefaultProfile</span></span>
<span data-ttu-id="1bc3a-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bc3a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc3a-127">CommonParameters</span></span>
<span data-ttu-id="1bc3a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc3a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1bc3a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc3a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="1bc3a-130">INPUTS</span></span>

## <span data-ttu-id="1bc3a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1bc3a-131">OUTPUTS</span></span>

### <span data-ttu-id="1bc3a-132">bool</span><span class="sxs-lookup"><span data-stu-id="1bc3a-132">bool</span></span>

## <span data-ttu-id="1bc3a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1bc3a-133">NOTES</span></span>

## <span data-ttu-id="1bc3a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1bc3a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1bc3a-135">AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1bc3a-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="1bc3a-136">新-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1bc3a-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="1bc3a-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1bc3a-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


