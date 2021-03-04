---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 05f3ac10171c9135b59b9fb6894f5b5fbf670de0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904146"
---
# <span data-ttu-id="417c1-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="417c1-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="417c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="417c1-102">SYNOPSIS</span></span>
<span data-ttu-id="417c1-103">移除群組中的產品。</span><span class="sxs-lookup"><span data-stu-id="417c1-103">Removes a product from a group.</span></span>

## <span data-ttu-id="417c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="417c1-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="417c1-105">描述</span><span class="sxs-lookup"><span data-stu-id="417c1-105">DESCRIPTION</span></span>
<span data-ttu-id="417c1-106">**Remove-AzApiManagementProductFromGroup** Cmdlet 會移除現有群組中的產品。</span><span class="sxs-lookup"><span data-stu-id="417c1-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="417c1-107">換句話說，此 Cmdlet 會從產品移除群組指派。</span><span class="sxs-lookup"><span data-stu-id="417c1-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="417c1-108">例子</span><span class="sxs-lookup"><span data-stu-id="417c1-108">EXAMPLES</span></span>

### <span data-ttu-id="417c1-109">範例 1：從群組移除產品</span><span class="sxs-lookup"><span data-stu-id="417c1-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="417c1-110">此命令會移除現有群組中的產品。</span><span class="sxs-lookup"><span data-stu-id="417c1-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="417c1-111">參數</span><span class="sxs-lookup"><span data-stu-id="417c1-111">PARAMETERS</span></span>

### <span data-ttu-id="417c1-112">-內容</span><span class="sxs-lookup"><span data-stu-id="417c1-112">-Context</span></span>
<span data-ttu-id="417c1-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="417c1-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="417c1-114">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="417c1-114">This parameter is required.</span></span>

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

### <span data-ttu-id="417c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="417c1-115">-DefaultProfile</span></span>
<span data-ttu-id="417c1-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="417c1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="417c1-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="417c1-117">-GroupId</span></span>
<span data-ttu-id="417c1-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="417c1-118">Specifies the group ID.</span></span>
<span data-ttu-id="417c1-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="417c1-119">This parameter is required.</span></span>

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

### <span data-ttu-id="417c1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="417c1-120">-PassThru</span></span>
<span data-ttu-id="417c1-121">表示此 Cmdlet 會$True ，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="417c1-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="417c1-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="417c1-122">-ProductId</span></span>
<span data-ttu-id="417c1-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="417c1-123">Specifies the product ID.</span></span>
<span data-ttu-id="417c1-124">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="417c1-124">This parameter is required.</span></span>

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

### <span data-ttu-id="417c1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="417c1-125">CommonParameters</span></span>
<span data-ttu-id="417c1-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="417c1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="417c1-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="417c1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="417c1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="417c1-128">INPUTS</span></span>

### <span data-ttu-id="417c1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="417c1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="417c1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="417c1-130">System.String</span></span>

### <span data-ttu-id="417c1-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="417c1-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="417c1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="417c1-132">OUTPUTS</span></span>

### <span data-ttu-id="417c1-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="417c1-133">System.Boolean</span></span>

## <span data-ttu-id="417c1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="417c1-134">NOTES</span></span>

## <span data-ttu-id="417c1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="417c1-135">RELATED LINKS</span></span>

[<span data-ttu-id="417c1-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="417c1-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


