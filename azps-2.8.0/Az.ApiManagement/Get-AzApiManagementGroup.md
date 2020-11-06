---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGroup.md
ms.openlocfilehash: 9a8acd17f953e90cd5b4311854830da03dc4df0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614055"
---
# <span data-ttu-id="11177-101">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="11177-101">Get-AzApiManagementGroup</span></span>

## <span data-ttu-id="11177-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11177-102">SYNOPSIS</span></span>
<span data-ttu-id="11177-103">取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="11177-103">Gets all or specific API management groups.</span></span>

## <span data-ttu-id="11177-104">句法</span><span class="sxs-lookup"><span data-stu-id="11177-104">SYNTAX</span></span>

### <span data-ttu-id="11177-105">GetAllGroups (預設) </span><span class="sxs-lookup"><span data-stu-id="11177-105">GetAllGroups (Default)</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11177-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="11177-106">GetByGroupId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11177-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="11177-107">GetByUserId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11177-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="11177-108">GetByProductId</span></span>
```
Get-AzApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11177-109">說明</span><span class="sxs-lookup"><span data-stu-id="11177-109">DESCRIPTION</span></span>
<span data-ttu-id="11177-110">**AzApiManagementGroup** Cmdlet 會取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="11177-110">The **Get-AzApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="11177-111">示例</span><span class="sxs-lookup"><span data-stu-id="11177-111">EXAMPLES</span></span>

### <span data-ttu-id="11177-112">範例1：取得所有群組</span><span class="sxs-lookup"><span data-stu-id="11177-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext
```

<span data-ttu-id="11177-113">這個命令會取得所有群組。</span><span class="sxs-lookup"><span data-stu-id="11177-113">This command gets all groups.</span></span>

### <span data-ttu-id="11177-114">範例2：透過識別碼取得群組</span><span class="sxs-lookup"><span data-stu-id="11177-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="11177-115">這個命令會取得名為0123456789的群組 ID。</span><span class="sxs-lookup"><span data-stu-id="11177-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="11177-116">範例3：依名稱取得群組</span><span class="sxs-lookup"><span data-stu-id="11177-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="11177-117">這個命令會取得名為 Group0002 的群組。</span><span class="sxs-lookup"><span data-stu-id="11177-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="11177-118">範例4：取得所有使用者群組</span><span class="sxs-lookup"><span data-stu-id="11177-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="11177-119">這個命令會取得使用者 ID 為0123456789的所有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="11177-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="11177-120">參數</span><span class="sxs-lookup"><span data-stu-id="11177-120">PARAMETERS</span></span>

### <span data-ttu-id="11177-121">-內容</span><span class="sxs-lookup"><span data-stu-id="11177-121">-Context</span></span>
<span data-ttu-id="11177-122">指定 PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="11177-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="11177-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11177-123">-DefaultProfile</span></span>
<span data-ttu-id="11177-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11177-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11177-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="11177-125">-GroupId</span></span>
<span data-ttu-id="11177-126">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="11177-126">Specifies the group ID.</span></span>
<span data-ttu-id="11177-127">如果已指定，此 Cmdlet 會嘗試透過識別碼尋找群組。</span><span class="sxs-lookup"><span data-stu-id="11177-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

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

### <span data-ttu-id="11177-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="11177-128">-Name</span></span>
<span data-ttu-id="11177-129">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11177-129">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="11177-130">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="11177-130">-ProductId</span></span>
<span data-ttu-id="11177-131">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11177-131">Identifier of existing product.</span></span>
<span data-ttu-id="11177-132">如果已指定，將會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="11177-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="11177-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="11177-133">This parameter is optional.</span></span>

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

### <span data-ttu-id="11177-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="11177-134">-UserId</span></span>
<span data-ttu-id="11177-135">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11177-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="11177-136">如果已指定 Cmdlet，則會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="11177-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

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

### <span data-ttu-id="11177-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11177-137">CommonParameters</span></span>
<span data-ttu-id="11177-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11177-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11177-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="11177-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11177-140">輸入</span><span class="sxs-lookup"><span data-stu-id="11177-140">INPUTS</span></span>

### <span data-ttu-id="11177-141">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="11177-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="11177-142">System.object</span><span class="sxs-lookup"><span data-stu-id="11177-142">System.String</span></span>

## <span data-ttu-id="11177-143">輸出</span><span class="sxs-lookup"><span data-stu-id="11177-143">OUTPUTS</span></span>

### <span data-ttu-id="11177-144">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="11177-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="11177-145">筆記</span><span class="sxs-lookup"><span data-stu-id="11177-145">NOTES</span></span>

## <span data-ttu-id="11177-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="11177-146">RELATED LINKS</span></span>

[<span data-ttu-id="11177-147">新-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="11177-147">New-AzApiManagementGroup</span></span>](./New-AzApiManagementGroup.md)

[<span data-ttu-id="11177-148">移除-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="11177-148">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="11177-149">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="11177-149">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)

