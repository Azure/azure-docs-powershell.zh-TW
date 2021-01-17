---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 4c90b51a316db63bad2e5481e1b6390849d83292
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287700"
---
# <span data-ttu-id="4da33-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4da33-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="4da33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4da33-102">SYNOPSIS</span></span>
<span data-ttu-id="4da33-103">刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="4da33-103">Deletes an existing user.</span></span>

## <span data-ttu-id="4da33-104">句法</span><span class="sxs-lookup"><span data-stu-id="4da33-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4da33-105">說明</span><span class="sxs-lookup"><span data-stu-id="4da33-105">DESCRIPTION</span></span>
<span data-ttu-id="4da33-106">**AzApiManagementUser** Cmdlet 會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="4da33-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="4da33-107">示例</span><span class="sxs-lookup"><span data-stu-id="4da33-107">EXAMPLES</span></span>

### <span data-ttu-id="4da33-108">範例1：刪除使用者</span><span class="sxs-lookup"><span data-stu-id="4da33-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="4da33-109">這個命令會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="4da33-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="4da33-110">參數</span><span class="sxs-lookup"><span data-stu-id="4da33-110">PARAMETERS</span></span>

### <span data-ttu-id="4da33-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4da33-111">-Context</span></span>
<span data-ttu-id="4da33-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4da33-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="4da33-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="4da33-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4da33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da33-114">-DefaultProfile</span></span>
<span data-ttu-id="4da33-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4da33-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4da33-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="4da33-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="4da33-117">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="4da33-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="4da33-118">如果未指定此參數且已存在訂閱，則此 Cmdlet 會引發例外狀況。</span><span class="sxs-lookup"><span data-stu-id="4da33-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="4da33-119">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="4da33-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="4da33-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4da33-120">-PassThru</span></span>
<span data-ttu-id="4da33-121">指示這個 Cmdlet 會傳回 $Ture 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="4da33-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="4da33-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="4da33-122">-UserId</span></span>
<span data-ttu-id="4da33-123">指定要移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="4da33-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="4da33-124">-確認</span><span class="sxs-lookup"><span data-stu-id="4da33-124">-Confirm</span></span>
<span data-ttu-id="4da33-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4da33-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da33-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da33-126">-WhatIf</span></span>
<span data-ttu-id="4da33-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4da33-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da33-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4da33-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da33-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da33-129">CommonParameters</span></span>
<span data-ttu-id="4da33-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4da33-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da33-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4da33-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da33-132">輸入</span><span class="sxs-lookup"><span data-stu-id="4da33-132">INPUTS</span></span>

### <span data-ttu-id="4da33-133">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4da33-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4da33-134">System.object</span><span class="sxs-lookup"><span data-stu-id="4da33-134">System.String</span></span>

### <span data-ttu-id="4da33-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4da33-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4da33-136">輸出</span><span class="sxs-lookup"><span data-stu-id="4da33-136">OUTPUTS</span></span>

### <span data-ttu-id="4da33-137">System.object</span><span class="sxs-lookup"><span data-stu-id="4da33-137">System.Boolean</span></span>

## <span data-ttu-id="4da33-138">筆記</span><span class="sxs-lookup"><span data-stu-id="4da33-138">NOTES</span></span>

## <span data-ttu-id="4da33-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="4da33-139">RELATED LINKS</span></span>

[<span data-ttu-id="4da33-140">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4da33-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="4da33-141">新-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4da33-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="4da33-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="4da33-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


