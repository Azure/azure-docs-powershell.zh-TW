---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EEB52CCA-F5D6-4ACB-A6C9-D07C510A5878
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0c28742eb3c774adb8c7b6a8d920e91377bea35f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450932"
---
# <span data-ttu-id="307cf-101">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="307cf-101">Get-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="307cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="307cf-102">SYNOPSIS</span></span>
<span data-ttu-id="307cf-103">取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-103">Gets all or specific API management groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="307cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="307cf-104">SYNTAX</span></span>

### <span data-ttu-id="307cf-105"> (預設) 取得所有群組</span><span class="sxs-lookup"><span data-stu-id="307cf-105">Get all groups (Default)</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307cf-106">依群組識別碼取得</span><span class="sxs-lookup"><span data-stu-id="307cf-106">Get by group ID</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307cf-107">依使用者尋找群組</span><span class="sxs-lookup"><span data-stu-id="307cf-107">Find groups by user</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="307cf-108">依產品尋找群組</span><span class="sxs-lookup"><span data-stu-id="307cf-108">Find groups by product</span></span>
```
Get-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-Name <String>] [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="307cf-109">說明</span><span class="sxs-lookup"><span data-stu-id="307cf-109">DESCRIPTION</span></span>
<span data-ttu-id="307cf-110">**AzureRmApiManagementGroup** Cmdlet 會取得全部或特定的 API 管理群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-110">The **Get-AzureRmApiManagementGroup** cmdlet gets all or specific API management groups.</span></span>

## <span data-ttu-id="307cf-111">示例</span><span class="sxs-lookup"><span data-stu-id="307cf-111">EXAMPLES</span></span>

### <span data-ttu-id="307cf-112">範例1：取得所有群組</span><span class="sxs-lookup"><span data-stu-id="307cf-112">Example 1: Get all groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext
```

<span data-ttu-id="307cf-113">這個命令會取得所有群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-113">This command gets all groups.</span></span>

### <span data-ttu-id="307cf-114">範例2：透過識別碼取得群組</span><span class="sxs-lookup"><span data-stu-id="307cf-114">Example 2: Get a group by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -GroupId "0123456789"
```

<span data-ttu-id="307cf-115">這個命令會取得名為0123456789的群組 ID。</span><span class="sxs-lookup"><span data-stu-id="307cf-115">This command gets  the group ID named 0123456789.</span></span>

### <span data-ttu-id="307cf-116">範例3：依名稱取得群組</span><span class="sxs-lookup"><span data-stu-id="307cf-116">Example 3: Get a group by name</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -Name "Group0002"
```

<span data-ttu-id="307cf-117">這個命令會取得名為 Group0002 的群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-117">This command gets the group named Group0002.</span></span>

### <span data-ttu-id="307cf-118">範例4：取得所有使用者群組</span><span class="sxs-lookup"><span data-stu-id="307cf-118">Example 4: Get all user groups</span></span>
```
PS C:\>Get-AzureRmApiManagementGroup -Context $APImContext -UserId "0123456789"
```

<span data-ttu-id="307cf-119">這個命令會取得使用者 ID 為0123456789的所有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-119">This command gets all user groups with the user ID named 0123456789.</span></span>

## <span data-ttu-id="307cf-120">參數</span><span class="sxs-lookup"><span data-stu-id="307cf-120">PARAMETERS</span></span>

### <span data-ttu-id="307cf-121">-內容</span><span class="sxs-lookup"><span data-stu-id="307cf-121">-Context</span></span>
<span data-ttu-id="307cf-122">指定 PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="307cf-122">Specifies an instance of PsApiManagementContext.</span></span>

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

### <span data-ttu-id="307cf-123">-GroupId</span><span class="sxs-lookup"><span data-stu-id="307cf-123">-GroupId</span></span>
<span data-ttu-id="307cf-124">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="307cf-124">Specifies the group ID.</span></span>
<span data-ttu-id="307cf-125">如果已指定，此 Cmdlet 會嘗試透過識別碼尋找群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-125">If specified, the cmdlet attempts to find the group by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by group ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307cf-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="307cf-126">-Name</span></span>
<span data-ttu-id="307cf-127">指定管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="307cf-127">Specifies the name of the management group.</span></span>

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

### <span data-ttu-id="307cf-128">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="307cf-128">-ProductId</span></span>
<span data-ttu-id="307cf-129">現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="307cf-129">Identifier of existing product.</span></span>
<span data-ttu-id="307cf-130">如果已指定，將會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-130">If specified will return all groups the product assigned to.</span></span>
<span data-ttu-id="307cf-131">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="307cf-131">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by product
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307cf-132">-UserId</span><span class="sxs-lookup"><span data-stu-id="307cf-132">-UserId</span></span>
<span data-ttu-id="307cf-133">指定現有產品的識別碼。</span><span class="sxs-lookup"><span data-stu-id="307cf-133">Specifies the identifier of existing product.</span></span>
<span data-ttu-id="307cf-134">如果已指定 Cmdlet，則會傳回指派給該產品的所有群組。</span><span class="sxs-lookup"><span data-stu-id="307cf-134">If specified the cmdlet will return all groups the product assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: Find groups by user
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="307cf-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="307cf-135">-DefaultProfile</span></span>
<span data-ttu-id="307cf-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="307cf-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="307cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="307cf-137">CommonParameters</span></span>
<span data-ttu-id="307cf-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="307cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="307cf-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="307cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="307cf-140">輸入</span><span class="sxs-lookup"><span data-stu-id="307cf-140">INPUTS</span></span>

## <span data-ttu-id="307cf-141">輸出</span><span class="sxs-lookup"><span data-stu-id="307cf-141">OUTPUTS</span></span>

### <span data-ttu-id="307cf-142">IList<ApiManagement. ServiceManagement. PsApiManagementGroup]></span><span class="sxs-lookup"><span data-stu-id="307cf-142">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup></span></span>

## <span data-ttu-id="307cf-143">筆記</span><span class="sxs-lookup"><span data-stu-id="307cf-143">NOTES</span></span>

## <span data-ttu-id="307cf-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="307cf-144">RELATED LINKS</span></span>

[<span data-ttu-id="307cf-145">新-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="307cf-145">New-AzureRmApiManagementGroup</span></span>](./New-AzureRmApiManagementGroup.md)

[<span data-ttu-id="307cf-146">移除-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="307cf-146">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="307cf-147">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="307cf-147">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)


