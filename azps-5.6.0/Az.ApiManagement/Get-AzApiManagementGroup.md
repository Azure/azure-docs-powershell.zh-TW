---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 786d095b7750843688b4319eec7e46263332a4c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904154"
---
# <span data-ttu-id="1c2b7-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c2b7-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="1c2b7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1c2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="1c2b7-103">獲得所有或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="1c2b7-104">語法</span><span class="sxs-lookup"><span data-stu-id="1c2b7-104">SYNTAX</span></span>

### <span data-ttu-id="1c2b7-105">GetAllGroups (預設) </span><span class="sxs-lookup"><span data-stu-id="1c2b7-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2b7-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2b7-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c2b7-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c2b7-109">描述</span><span class="sxs-lookup"><span data-stu-id="1c2b7-109">DESCRIPTION</span></span>
<span data-ttu-id="1c2b7-110">**Get-AzApiManagementGroup** Cmdlet 會取得所有或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="1c2b7-111">例子</span><span class="sxs-lookup"><span data-stu-id="1c2b7-111">EXAMPLES</span></span>

### <span data-ttu-id="1c2b7-112">範例 1：取得所有群組</span><span class="sxs-lookup"><span data-stu-id="1c2b7-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="1c2b7-113">此命令會獲得所有群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-113">This command gets all groups.</span></span>

### <span data-ttu-id="1c2b7-114">範例 2：根據識別碼取得群組</span><span class="sxs-lookup"><span data-stu-id="1c2b7-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="1c2b7-115">此命令會獲得名為 0123456789 的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="1c2b7-116">範例 3：按名稱取得群組</span><span class="sxs-lookup"><span data-stu-id="1c2b7-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="1c2b7-117">此命令會獲得名為 Group0002 的群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="1c2b7-118">範例 4：取得所有使用者群組</span><span class="sxs-lookup"><span data-stu-id="1c2b7-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="1c2b7-119">此命令會獲得使用者識別碼為 0123456789 的所有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="1c2b7-120">參數</span><span class="sxs-lookup"><span data-stu-id="1c2b7-120">PARAMETERS</span></span>

### <span data-ttu-id="1c2b7-121">-內容</span><span class="sxs-lookup"><span data-stu-id="1c2b7-121">-Context</span></span>
<span data-ttu-id="1c2b7-122">指定 PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="1c2b7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c2b7-123">-DefaultProfile</span></span>
<span data-ttu-id="1c2b7-124">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c2b7-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-125">-GroupId</span></span>
<span data-ttu-id="1c2b7-126">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-126">Specifies the group ID.</span></span>
<span data-ttu-id="1c2b7-127">如果指定，Cmdlet 會嘗試根據識別碼尋找群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGroupId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2b7-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="1c2b7-128">-Name</span></span>
<span data-ttu-id="1c2b7-129">指定管理組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-129">Specifies the name of the management group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2b7-130">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-130">-ProductId</span></span>
<span data-ttu-id="1c2b7-131">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-131">Identifier of existing product.</span></span>
<span data-ttu-id="1c2b7-132">如果指定，會退回產品指派給的所有群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="1c2b7-133">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2b7-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="1c2b7-134">-UserId</span></span>
<span data-ttu-id="1c2b7-135">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="1c2b7-136">如果指定，Cmdlet 會返回產品指派給的所有群組。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c2b7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c2b7-137">CommonParameters</span></span>
<span data-ttu-id="1c2b7-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1c2b7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c2b7-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c2b7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c2b7-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1c2b7-140">INPUTS</span></span>

### <span data-ttu-id="1c2b7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="1c2b7-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c2b7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1c2b7-142">System.String</span></span>

## <span data-ttu-id="1c2b7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1c2b7-143">OUTPUTS</span></span>

### <span data-ttu-id="1c2b7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c2b7-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="1c2b7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1c2b7-145">NOTES</span></span>

## <span data-ttu-id="1c2b7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c2b7-146">RELATED LINKS</span></span>

[<span data-ttu-id="1c2b7-147">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c2b7-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="1c2b7-148">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c2b7-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="1c2b7-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c2b7-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)


