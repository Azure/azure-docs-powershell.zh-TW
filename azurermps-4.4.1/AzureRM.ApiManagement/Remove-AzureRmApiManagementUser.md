---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445168"
---
# <span data-ttu-id="24cbd-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="24cbd-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="24cbd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="24cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="24cbd-103">刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="24cbd-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24cbd-104">句法</span><span class="sxs-lookup"><span data-stu-id="24cbd-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24cbd-105">說明</span><span class="sxs-lookup"><span data-stu-id="24cbd-105">DESCRIPTION</span></span>
<span data-ttu-id="24cbd-106">**AzureRmApiManagementUser** Cmdlet 會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="24cbd-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="24cbd-107">示例</span><span class="sxs-lookup"><span data-stu-id="24cbd-107">EXAMPLES</span></span>

### <span data-ttu-id="24cbd-108">範例1：刪除使用者</span><span class="sxs-lookup"><span data-stu-id="24cbd-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="24cbd-109">這個命令會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="24cbd-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="24cbd-110">參數</span><span class="sxs-lookup"><span data-stu-id="24cbd-110">PARAMETERS</span></span>

### <span data-ttu-id="24cbd-111">-內容</span><span class="sxs-lookup"><span data-stu-id="24cbd-111">-Context</span></span>
<span data-ttu-id="24cbd-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="24cbd-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="24cbd-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="24cbd-113">This parameter is required.</span></span>

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

### <span data-ttu-id="24cbd-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="24cbd-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="24cbd-115">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="24cbd-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="24cbd-116">如果未指定此參數且已存在訂閱，則此 Cmdlet 會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="24cbd-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="24cbd-117">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="24cbd-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="24cbd-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24cbd-118">-PassThru</span></span>
<span data-ttu-id="24cbd-119">指示這個 Cmdlet 會傳回 $Ture 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="24cbd-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="24cbd-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="24cbd-120">-UserId</span></span>
<span data-ttu-id="24cbd-121">指定要移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="24cbd-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="24cbd-122">-確認</span><span class="sxs-lookup"><span data-stu-id="24cbd-122">-Confirm</span></span>
<span data-ttu-id="24cbd-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="24cbd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24cbd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24cbd-124">-WhatIf</span></span>
<span data-ttu-id="24cbd-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="24cbd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24cbd-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="24cbd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24cbd-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24cbd-127">-DefaultProfile</span></span>
<span data-ttu-id="24cbd-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="24cbd-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24cbd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24cbd-129">CommonParameters</span></span>
<span data-ttu-id="24cbd-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="24cbd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24cbd-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="24cbd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24cbd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="24cbd-132">INPUTS</span></span>

## <span data-ttu-id="24cbd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="24cbd-133">OUTPUTS</span></span>

### <span data-ttu-id="24cbd-134">布林值</span><span class="sxs-lookup"><span data-stu-id="24cbd-134">Boolean</span></span>

## <span data-ttu-id="24cbd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="24cbd-135">NOTES</span></span>

## <span data-ttu-id="24cbd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="24cbd-136">RELATED LINKS</span></span>

[<span data-ttu-id="24cbd-137">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="24cbd-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="24cbd-138">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="24cbd-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="24cbd-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="24cbd-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


