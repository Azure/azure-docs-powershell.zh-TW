---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUser.md
ms.openlocfilehash: 17f7fe4046d5de9dfe288a96a00e8c03486e9c61
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903682"
---
# <span data-ttu-id="f8c69-101">Remove-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f8c69-101">Remove-AzApiManagementUser</span></span>

## <span data-ttu-id="f8c69-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f8c69-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c69-103">刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="f8c69-103">Deletes an existing user.</span></span>

## <span data-ttu-id="f8c69-104">語法</span><span class="sxs-lookup"><span data-stu-id="f8c69-104">SYNTAX</span></span>

```
Remove-AzApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c69-105">描述</span><span class="sxs-lookup"><span data-stu-id="f8c69-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c69-106">**Remove-AzApiManagementUser** Cmdlet 會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="f8c69-106">The **Remove-AzApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="f8c69-107">例子</span><span class="sxs-lookup"><span data-stu-id="f8c69-107">EXAMPLES</span></span>

### <span data-ttu-id="f8c69-108">範例 1：刪除使用者</span><span class="sxs-lookup"><span data-stu-id="f8c69-108">Example 1: Delete a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="f8c69-109">此命令會刪除現有的使用者。</span><span class="sxs-lookup"><span data-stu-id="f8c69-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="f8c69-110">參數</span><span class="sxs-lookup"><span data-stu-id="f8c69-110">PARAMETERS</span></span>

### <span data-ttu-id="f8c69-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f8c69-111">-Context</span></span>
<span data-ttu-id="f8c69-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f8c69-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f8c69-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="f8c69-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f8c69-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c69-114">-DefaultProfile</span></span>
<span data-ttu-id="f8c69-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8c69-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8c69-116">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="f8c69-116">-DeleteSubscriptions</span></span>
<span data-ttu-id="f8c69-117">指出是否要刪除產品的訂閱。</span><span class="sxs-lookup"><span data-stu-id="f8c69-117">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="f8c69-118">如果未指定此參數且有訂閱存在，此 Cmdlet 會放棄例外。</span><span class="sxs-lookup"><span data-stu-id="f8c69-118">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="f8c69-119">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="f8c69-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="f8c69-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8c69-120">-PassThru</span></span>
<span data-ttu-id="f8c69-121">表示此 Cmdlet 會$Ture值 ，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="f8c69-121">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f8c69-122">-UserId</span><span class="sxs-lookup"><span data-stu-id="f8c69-122">-UserId</span></span>
<span data-ttu-id="f8c69-123">指定要移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f8c69-123">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="f8c69-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f8c69-124">-Confirm</span></span>
<span data-ttu-id="f8c69-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f8c69-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c69-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c69-126">-WhatIf</span></span>
<span data-ttu-id="f8c69-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f8c69-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c69-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f8c69-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c69-129">CommonParameters</span></span>
<span data-ttu-id="f8c69-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f8c69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c69-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8c69-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c69-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f8c69-132">INPUTS</span></span>

### <span data-ttu-id="f8c69-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="f8c69-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f8c69-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f8c69-134">System.String</span></span>

### <span data-ttu-id="f8c69-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8c69-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f8c69-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f8c69-136">OUTPUTS</span></span>

### <span data-ttu-id="f8c69-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8c69-137">System.Boolean</span></span>

## <span data-ttu-id="f8c69-138">筆記</span><span class="sxs-lookup"><span data-stu-id="f8c69-138">NOTES</span></span>

## <span data-ttu-id="f8c69-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f8c69-139">RELATED LINKS</span></span>

[<span data-ttu-id="f8c69-140">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f8c69-140">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="f8c69-141">New-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f8c69-141">New-AzApiManagementUser</span></span>](./New-AzApiManagementUser.md)

[<span data-ttu-id="f8c69-142">Set-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f8c69-142">Set-AzApiManagementUser</span></span>](./Set-AzApiManagementUser.md)


