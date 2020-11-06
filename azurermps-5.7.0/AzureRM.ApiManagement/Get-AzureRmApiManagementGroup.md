---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: b77452bff93a9b66f8ffe54fdff623d391749622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452284"
---
# <span data-ttu-id="27972-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27972-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="27972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="27972-102">SYNOPSIS</span></span>
<span data-ttu-id="27972-103">取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="27972-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27972-104">句法</span><span class="sxs-lookup"><span data-stu-id="27972-104">SYNTAX</span></span>

### <span data-ttu-id="27972-105">GetAllGroups (預設) </span><span class="sxs-lookup"><span data-stu-id="27972-105">GetAllGroups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27972-106">GetByGroupId</span><span class="sxs-lookup"><span data-stu-id="27972-106">GetByGroupId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27972-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="27972-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27972-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="27972-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27972-109">說明</span><span class="sxs-lookup"><span data-stu-id="27972-109">DESCRIPTION</span></span>
<span data-ttu-id="27972-110">**AzureRmApiManagementGroup** Cmdlet 會取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="27972-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="27972-111">示例</span><span class="sxs-lookup"><span data-stu-id="27972-111">EXAMPLES</span></span>

### <span data-ttu-id="27972-112">範例1：取得所有群組</span><span class="sxs-lookup"><span data-stu-id="27972-112">Example 1: Get all groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext
```

<span data-ttu-id="27972-113">這個命令會取得所有群組。</span><span class="sxs-lookup"><span data-stu-id="27972-113">This command gets all groups.</span></span>

### <span data-ttu-id="27972-114">範例2：透過識別碼取得群組</span><span class="sxs-lookup"><span data-stu-id="27972-114">Example 2: Get a group by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -GroupId "0123456789"
```

<span data-ttu-id="27972-115">這個命令會取得名為0123456789的群組 ID。</span><span class="sxs-lookup"><span data-stu-id="27972-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="27972-116">範例3：依名稱取得群組</span><span class="sxs-lookup"><span data-stu-id="27972-116">Example 3: Get a group by name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -Name "Group0002"
```

<span data-ttu-id="27972-117">這個命令會取得名為 Group0002 的群組。</span><span class="sxs-lookup"><span data-stu-id="27972-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="27972-118">範例4：取得所有使用者群組</span><span class="sxs-lookup"><span data-stu-id="27972-118">Example 4: Get all user groups</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementGroup -Context $apimContext -UserId "0123456789"
```

<span data-ttu-id="27972-119">這個命令會取得使用者 ID 為0123456789的所有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="27972-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="27972-120">參數</span><span class="sxs-lookup"><span data-stu-id="27972-120">PARAMETERS</span></span>

### <span data-ttu-id="27972-121">-內容</span><span class="sxs-lookup"><span data-stu-id="27972-121">-Context</span></span>
<span data-ttu-id="27972-122">指定 PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="27972-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="27972-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27972-123">-DefaultProfile</span></span>
<span data-ttu-id="27972-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="27972-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="27972-125">-GroupId</span><span class="sxs-lookup"><span data-stu-id="27972-125">-GroupId</span></span>
<span data-ttu-id="27972-126">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="27972-126">Specifies the group ID.</span></span>
<span data-ttu-id="27972-127">如果已指定，此 Cmdlet 會嘗試透過識別碼尋找群組。</span><span class="sxs-lookup"><span data-stu-id="27972-127">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByGroupId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27972-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="27972-128">-Name</span></span>
<span data-ttu-id="27972-129">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="27972-129">Specifies the name of the management group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27972-130">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="27972-130">-ProductId</span></span>
<span data-ttu-id="27972-131">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27972-131">Identifier of existing product.</span></span>
<span data-ttu-id="27972-132">如果已指定，將會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="27972-132">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="27972-133">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="27972-133">This parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27972-134">-UserId</span><span class="sxs-lookup"><span data-stu-id="27972-134">-UserId</span></span>
<span data-ttu-id="27972-135">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="27972-135">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="27972-136">如果已指定 Cmdlet，則會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="27972-136">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27972-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27972-137">CommonParameters</span></span>
<span data-ttu-id="27972-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="27972-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27972-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="27972-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27972-140">輸入</span><span class="sxs-lookup"><span data-stu-id="27972-140">INPUTS</span></span>

### <span data-ttu-id="27972-141">所有</span><span class="sxs-lookup"><span data-stu-id="27972-141">None</span></span>
<span data-ttu-id="27972-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="27972-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27972-143">輸出</span><span class="sxs-lookup"><span data-stu-id="27972-143">OUTPUTS</span></span>

### <span data-ttu-id="27972-144">ServiceManagement. PsApiManagementGroup （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="27972-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>
<span data-ttu-id="27972-145">在 API 管理服務中設定之群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="27972-145">The details of the Group configured in API Management service.</span></span>

### <span data-ttu-id="27972-146">IList<ApiManagement. ServiceManagement. PsApiManagementGroup]></span><span class="sxs-lookup"><span data-stu-id="27972-146">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>
<span data-ttu-id="27972-147">在 API 管理服務中設定的群組清單。</span><span class="sxs-lookup"><span data-stu-id="27972-147">The list of Groups configured in API Management service.</span></span>

## <span data-ttu-id="27972-148">筆記</span><span class="sxs-lookup"><span data-stu-id="27972-148">NOTES</span></span>

## <span data-ttu-id="27972-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="27972-149">RELATED LINKS</span></span>

[<span data-ttu-id="27972-150">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27972-150">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="27972-151">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27972-151">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="27972-152">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="27972-152">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


