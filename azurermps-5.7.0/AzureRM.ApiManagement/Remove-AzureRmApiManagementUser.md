---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 5d657610ddce1c0397a5f9e8c11b832b3fcd472b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626570"
---
# <span data-ttu-id="2bf2e-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2bf2e-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="2bf2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2bf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf2e-103">刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bf2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2bf2e-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2bf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf2e-106">**AzureRmApiManagementUser** Cmdlet 會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="2bf2e-107">示例</span><span class="sxs-lookup"><span data-stu-id="2bf2e-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf2e-108">範例1：刪除使用者</span><span class="sxs-lookup"><span data-stu-id="2bf2e-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="2bf2e-109">這個命令會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="2bf2e-110">參數</span><span class="sxs-lookup"><span data-stu-id="2bf2e-110">PARAMETERS</span></span>

### <span data-ttu-id="2bf2e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="2bf2e-111">-Context</span></span>
<span data-ttu-id="2bf2e-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="2bf2e-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2bf2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf2e-114">-DefaultProfile</span></span>
<span data-ttu-id="2bf2e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2bf2e-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="2bf2e-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="2bf2e-117">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="2bf2e-118">如果未指定此參數且已存在訂閱，則此 Cmdlet 會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="2bf2e-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="2bf2e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bf2e-120">-PassThru</span></span>
<span data-ttu-id="2bf2e-121">指示這個 Cmdlet 會傳回 $Ture 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="2bf2e-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="2bf2e-122">-UserId</span></span>
<span data-ttu-id="2bf2e-123">指定要移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="2bf2e-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2bf2e-124">-Confirm</span></span>
<span data-ttu-id="2bf2e-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf2e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf2e-126">-WhatIf</span></span>
<span data-ttu-id="2bf2e-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf2e-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf2e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf2e-129">CommonParameters</span></span>
<span data-ttu-id="2bf2e-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf2e-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf2e-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2bf2e-132">INPUTS</span></span>

### <span data-ttu-id="2bf2e-133">所有</span><span class="sxs-lookup"><span data-stu-id="2bf2e-133">None</span></span>
<span data-ttu-id="2bf2e-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2bf2e-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2bf2e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2bf2e-135">OUTPUTS</span></span>

### <span data-ttu-id="2bf2e-136">布林值</span><span class="sxs-lookup"><span data-stu-id="2bf2e-136">Boolean</span></span>

## <span data-ttu-id="2bf2e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2bf2e-137">NOTES</span></span>

## <span data-ttu-id="2bf2e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2bf2e-138">RELATED LINKS</span></span>

[<span data-ttu-id="2bf2e-139">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2bf2e-139">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="2bf2e-140">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2bf2e-140">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="2bf2e-141">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="2bf2e-141">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)

