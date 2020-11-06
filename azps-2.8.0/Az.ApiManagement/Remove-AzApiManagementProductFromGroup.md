---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 51f4caf679cf2440165e1808c152162d1f272d05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613912"
---
# <span data-ttu-id="5a357-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="5a357-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="5a357-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a357-102">SYNOPSIS</span></span>
<span data-ttu-id="5a357-103">從群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="5a357-103">Removes a product from a group.</span></span>

## <span data-ttu-id="5a357-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a357-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a357-105">說明</span><span class="sxs-lookup"><span data-stu-id="5a357-105">DESCRIPTION</span></span>
<span data-ttu-id="5a357-106">**AzApiManagementProductFromGroup** Cmdlet 會從現有的群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="5a357-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="5a357-107">換句話說，這個 Cmdlet 會將群組指派從產品中移除。</span><span class="sxs-lookup"><span data-stu-id="5a357-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="5a357-108">示例</span><span class="sxs-lookup"><span data-stu-id="5a357-108">EXAMPLES</span></span>

### <span data-ttu-id="5a357-109">範例1：從群組中移除產品</span><span class="sxs-lookup"><span data-stu-id="5a357-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="5a357-110">這個命令會從現有的群組中移除產品。</span><span class="sxs-lookup"><span data-stu-id="5a357-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="5a357-111">參數</span><span class="sxs-lookup"><span data-stu-id="5a357-111">PARAMETERS</span></span>

### <span data-ttu-id="5a357-112">-內容</span><span class="sxs-lookup"><span data-stu-id="5a357-112">-Context</span></span>
<span data-ttu-id="5a357-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="5a357-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="5a357-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5a357-114">This parameter is required.</span></span>

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

### <span data-ttu-id="5a357-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a357-115">-DefaultProfile</span></span>
<span data-ttu-id="5a357-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5a357-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a357-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="5a357-117">-GroupId</span></span>
<span data-ttu-id="5a357-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a357-118">Specifies the group ID.</span></span>
<span data-ttu-id="5a357-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5a357-119">This parameter is required.</span></span>

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

### <span data-ttu-id="5a357-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a357-120">-PassThru</span></span>
<span data-ttu-id="5a357-121">指出這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False。</span><span class="sxs-lookup"><span data-stu-id="5a357-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="5a357-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="5a357-122">-ProductId</span></span>
<span data-ttu-id="5a357-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a357-123">Specifies the product ID.</span></span>
<span data-ttu-id="5a357-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="5a357-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5a357-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a357-125">CommonParameters</span></span>
<span data-ttu-id="5a357-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a357-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a357-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a357-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a357-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5a357-128">INPUTS</span></span>

### <span data-ttu-id="5a357-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="5a357-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a357-130">System.object</span><span class="sxs-lookup"><span data-stu-id="5a357-130">System.String</span></span>

### <span data-ttu-id="5a357-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5a357-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a357-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5a357-132">OUTPUTS</span></span>

### <span data-ttu-id="5a357-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5a357-133">System.Boolean</span></span>

## <span data-ttu-id="5a357-134">筆記</span><span class="sxs-lookup"><span data-stu-id="5a357-134">NOTES</span></span>

## <span data-ttu-id="5a357-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a357-135">RELATED LINKS</span></span>

[<span data-ttu-id="5a357-136">附加 AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="5a357-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


