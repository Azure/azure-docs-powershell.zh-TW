---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 31ab005953ea405dc8aac093f973a6e842974814
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452891"
---
# <span data-ttu-id="229b9-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="229b9-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="229b9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="229b9-102">SYNOPSIS</span></span>
<span data-ttu-id="229b9-103">刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="229b9-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="229b9-104">句法</span><span class="sxs-lookup"><span data-stu-id="229b9-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="229b9-105">說明</span><span class="sxs-lookup"><span data-stu-id="229b9-105">DESCRIPTION</span></span>
<span data-ttu-id="229b9-106">**AzureRmApiManagementUser** Cmdlet 會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="229b9-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="229b9-107">示例</span><span class="sxs-lookup"><span data-stu-id="229b9-107">EXAMPLES</span></span>

### <span data-ttu-id="229b9-108">範例1：刪除使用者</span><span class="sxs-lookup"><span data-stu-id="229b9-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="229b9-109">這個命令會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="229b9-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="229b9-110">參數</span><span class="sxs-lookup"><span data-stu-id="229b9-110">PARAMETERS</span></span>

### <span data-ttu-id="229b9-111">-內容</span><span class="sxs-lookup"><span data-stu-id="229b9-111">-Context</span></span>
<span data-ttu-id="229b9-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="229b9-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="229b9-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="229b9-113">This parameter is required.</span></span>

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

### <span data-ttu-id="229b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="229b9-114">-DefaultProfile</span></span>
<span data-ttu-id="229b9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="229b9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="229b9-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="229b9-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="229b9-117">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="229b9-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="229b9-118">如果未指定此參數且已存在訂閱，則此 Cmdlet 會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="229b9-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="229b9-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="229b9-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="229b9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="229b9-120">-PassThru</span></span>
<span data-ttu-id="229b9-121">指示這個 Cmdlet 會傳回 $Ture 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="229b9-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="229b9-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="229b9-122">-UserId</span></span>
<span data-ttu-id="229b9-123">指定要移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="229b9-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="229b9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="229b9-124">-Confirm</span></span>
<span data-ttu-id="229b9-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="229b9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="229b9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="229b9-126">-WhatIf</span></span>
<span data-ttu-id="229b9-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="229b9-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="229b9-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="229b9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="229b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="229b9-129">CommonParameters</span></span>
<span data-ttu-id="229b9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="229b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="229b9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="229b9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="229b9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="229b9-132">INPUTS</span></span>

### <span data-ttu-id="229b9-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="229b9-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="229b9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="229b9-134">System.String</span></span>

### <span data-ttu-id="229b9-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="229b9-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="229b9-136">輸出</span><span class="sxs-lookup"><span data-stu-id="229b9-136">OUTPUTS</span></span>

### <span data-ttu-id="229b9-137">System.object</span><span class="sxs-lookup"><span data-stu-id="229b9-137">System.Boolean</span></span>

## <span data-ttu-id="229b9-138">筆記</span><span class="sxs-lookup"><span data-stu-id="229b9-138">NOTES</span></span>

## <span data-ttu-id="229b9-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="229b9-139">RELATED LINKS</span></span>

[<span data-ttu-id="229b9-140">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="229b9-140">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="229b9-141">新-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="229b9-141">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="229b9-142">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="229b9-142">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


