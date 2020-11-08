---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementnamedvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementNamedValue.md
ms.openlocfilehash: 8d6d7174278d1f997c6a62e75eec4958f75b1d6c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969465"
---
# <span data-ttu-id="e69b4-101">Get-AzApiManagementNamedValue</span><span class="sxs-lookup"><span data-stu-id="e69b4-101">Get-AzApiManagementNamedValue</span></span>

## <span data-ttu-id="e69b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e69b4-102">SYNOPSIS</span></span>
<span data-ttu-id="e69b4-103">取得清單或特定的命名值。</span><span class="sxs-lookup"><span data-stu-id="e69b4-103">Gets a list or a particular Named Value.</span></span>

## <span data-ttu-id="e69b4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e69b4-104">SYNTAX</span></span>

### <span data-ttu-id="e69b4-105">GetAllNamedValues (預設) </span><span class="sxs-lookup"><span data-stu-id="e69b4-105">GetAllNamedValues (Default)</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e69b4-106">GetByNamedValueId</span><span class="sxs-lookup"><span data-stu-id="e69b4-106">GetByNamedValueId</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-NamedValueId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e69b4-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="e69b4-107">GetByName</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e69b4-108">GetByTag</span><span class="sxs-lookup"><span data-stu-id="e69b4-108">GetByTag</span></span>
```
Get-AzApiManagementNamedValue -Context <PsApiManagementContext> [-Tag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e69b4-109">說明</span><span class="sxs-lookup"><span data-stu-id="e69b4-109">DESCRIPTION</span></span>
<span data-ttu-id="e69b4-110">**AzApiManagementNamedValue** Cmdlet 會取得清單或特定的命名值。</span><span class="sxs-lookup"><span data-stu-id="e69b4-110">The **Get-AzApiManagementNamedValue** cmdlet gets a list or a particular named value.</span></span>
<span data-ttu-id="e69b4-111">如果指定的值標示為秘密，就不會將值包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="e69b4-111">Value will not be included into result details if the named value marked as a secret.</span></span> <span data-ttu-id="e69b4-112">若要取得機密值，請使用 **AzApiManagementNamedValueSecretValue** 。</span><span class="sxs-lookup"><span data-stu-id="e69b4-112">To get secret value, use **Get-AzApiManagementNamedValueSecretValue**.</span></span>

## <span data-ttu-id="e69b4-113">示例</span><span class="sxs-lookup"><span data-stu-id="e69b4-113">EXAMPLES</span></span>

### <span data-ttu-id="e69b4-114">範例1：透過名稱取得命名值</span><span class="sxs-lookup"><span data-stu-id="e69b4-114">Example 1: Get Named Value by name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementNamedValue -Context $apimContext -Name "sql-connectionstring"
```

<span data-ttu-id="e69b4-115">這個命令會在指定的值名稱中取得已命名的值詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e69b4-115">This command gets the named value details given the named value name.</span></span>

## <span data-ttu-id="e69b4-116">參數</span><span class="sxs-lookup"><span data-stu-id="e69b4-116">PARAMETERS</span></span>

### <span data-ttu-id="e69b4-117">-內容</span><span class="sxs-lookup"><span data-stu-id="e69b4-117">-Context</span></span>
<span data-ttu-id="e69b4-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="e69b4-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e69b4-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e69b4-119">This parameter is required.</span></span>

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

### <span data-ttu-id="e69b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69b4-120">-DefaultProfile</span></span>
<span data-ttu-id="e69b4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e69b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e69b4-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e69b4-122">-Name</span></span>
<span data-ttu-id="e69b4-123">尋找名稱中包含字串名稱的命名值。</span><span class="sxs-lookup"><span data-stu-id="e69b4-123">Finds named values with names containing the string Name.</span></span>
<span data-ttu-id="e69b4-124">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e69b4-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="e69b4-125">-NamedValueId</span><span class="sxs-lookup"><span data-stu-id="e69b4-125">-NamedValueId</span></span>
<span data-ttu-id="e69b4-126">命名值的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e69b4-126">Identifier of the named value.</span></span>
<span data-ttu-id="e69b4-127">如果已指定，將會嘗試透過識別碼尋找指名的值。</span><span class="sxs-lookup"><span data-stu-id="e69b4-127">If specified will try to find named value by the identifier.</span></span>
<span data-ttu-id="e69b4-128">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e69b4-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="e69b4-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="e69b4-129">-Tag</span></span>
<span data-ttu-id="e69b4-130">尋找與標籤相關聯的命名值。</span><span class="sxs-lookup"><span data-stu-id="e69b4-130">Finds named values associated with a Tag.</span></span>
<span data-ttu-id="e69b4-131">如果已指定，將會傳回與標籤相關的所有屬性。</span><span class="sxs-lookup"><span data-stu-id="e69b4-131">If specified will return all properties associated with a tag.</span></span>
<span data-ttu-id="e69b4-132">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="e69b4-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="e69b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69b4-133">CommonParameters</span></span>
<span data-ttu-id="e69b4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e69b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69b4-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e69b4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69b4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e69b4-136">INPUTS</span></span>

### <span data-ttu-id="e69b4-137">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e69b4-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e69b4-138">System.object</span><span class="sxs-lookup"><span data-stu-id="e69b4-138">System.String</span></span>

## <span data-ttu-id="e69b4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e69b4-139">OUTPUTS</span></span>

### <span data-ttu-id="e69b4-140">ServiceManagement. PsApiManagementNamedValue （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e69b4-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementNamedValue</span></span>

## <span data-ttu-id="e69b4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e69b4-141">NOTES</span></span>

## <span data-ttu-id="e69b4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e69b4-142">RELATED LINKS</span></span>