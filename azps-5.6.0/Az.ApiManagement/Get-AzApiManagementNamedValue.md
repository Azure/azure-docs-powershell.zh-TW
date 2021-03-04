---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 791bbe35b480fe9779712d33a37a999bb651a132
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906361"
---
# <span data-ttu-id="949ec-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="949ec-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="949ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="949ec-102">SYNOPSIS</span></span>
<span data-ttu-id="949ec-103">會獲得清單或特定的命名值。</span><span class="sxs-lookup"><span data-stu-id="949ec-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="949ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="949ec-104">SYNTAX</span></span>

### <span data-ttu-id="949ec-105">GetAllNamedValues (預設) </span><span class="sxs-lookup"><span data-stu-id="949ec-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="949ec-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="949ec-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949ec-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="949ec-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="949ec-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="949ec-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="949ec-109">描述</span><span class="sxs-lookup"><span data-stu-id="949ec-109">DESCRIPTION</span></span>
<span data-ttu-id="949ec-110">**Get-AzApiManagementNamedValue** Cmdlet 會取得清單或特定的具名值。</span><span class="sxs-lookup"><span data-stu-id="949ec-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="949ec-111">如果指定值標示為機密，值將不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="949ec-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="949ec-112">若要取得機密值，請使用 **Get-AzApiManagementNamedValueSecretValue。**</span><span class="sxs-lookup"><span data-stu-id="949ec-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="949ec-113">例子</span><span class="sxs-lookup"><span data-stu-id="949ec-113">EXAMPLES</span></span>

### <span data-ttu-id="949ec-114">範例 1：根據名稱取得命名值</span><span class="sxs-lookup"><span data-stu-id="949ec-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="949ec-115">此命令會獲得指定值名稱的命名值詳細資料。</span><span class="sxs-lookup"><span data-stu-id="949ec-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="949ec-116">參數</span><span class="sxs-lookup"><span data-stu-id="949ec-116">PARAMETERS</span></span>

### <span data-ttu-id="949ec-117">-內容</span><span class="sxs-lookup"><span data-stu-id="949ec-117">-Context</span></span>
<span data-ttu-id="949ec-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="949ec-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="949ec-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="949ec-119">This parameter is required.</span></span>

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

### <span data-ttu-id="949ec-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="949ec-120">-DefaultProfile</span></span>
<span data-ttu-id="949ec-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="949ec-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="949ec-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="949ec-122">-Name</span></span>
<span data-ttu-id="949ec-123">尋找名稱包含字串名稱的命名值。</span><span class="sxs-lookup"><span data-stu-id="949ec-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="949ec-124">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="949ec-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949ec-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="949ec-125">-NamedValueId</span></span>
<span data-ttu-id="949ec-126">已命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="949ec-126">Identifier of the named value.</span></span>
<span data-ttu-id="949ec-127">如果指定，會嘗試根據識別碼尋找已命名的值。</span><span class="sxs-lookup"><span data-stu-id="949ec-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="949ec-128">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="949ec-128">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNamedValueId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949ec-129">-標記</span><span class="sxs-lookup"><span data-stu-id="949ec-129">-Tag</span></span>
<span data-ttu-id="949ec-130">尋找與標記相關聯的命名值。</span><span class="sxs-lookup"><span data-stu-id="949ec-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="949ec-131">如果指定，會返回與標記相關聯的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="949ec-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="949ec-132">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="949ec-132">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTag
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="949ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="949ec-133">CommonParameters</span></span>
<span data-ttu-id="949ec-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="949ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="949ec-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="949ec-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="949ec-136">輸入</span><span class="sxs-lookup"><span data-stu-id="949ec-136">INPUTS</span></span>

### <span data-ttu-id="949ec-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="949ec-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="949ec-138">System.String</span><span class="sxs-lookup"><span data-stu-id="949ec-138">System.String</span></span>

## <span data-ttu-id="949ec-139">輸出</span><span class="sxs-lookup"><span data-stu-id="949ec-139">OUTPUTS</span></span>

### <span data-ttu-id="949ec-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="949ec-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="949ec-141">筆記</span><span class="sxs-lookup"><span data-stu-id="949ec-141">NOTES</span></span>

## <span data-ttu-id="949ec-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="949ec-142">RELATED LINKS</span></span>
