---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 545722e48095f8b77104bb6ff24b856bd76e3312
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407806"
---
# <span data-ttu-id="adc62-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="adc62-101">Get-AzADApplication</span></span>

## <span data-ttu-id="adc62-102">簡介</span><span class="sxs-lookup"><span data-stu-id="adc62-102">SYNOPSIS</span></span>
<span data-ttu-id="adc62-103">列出現有的 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="adc62-104">語法</span><span class="sxs-lookup"><span data-stu-id="adc62-104">SYNTAX</span></span>

### <span data-ttu-id="adc62-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="adc62-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="adc62-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc62-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="adc62-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc62-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="adc62-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc62-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="adc62-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc62-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="adc62-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="adc62-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="adc62-111">描述</span><span class="sxs-lookup"><span data-stu-id="adc62-111">DESCRIPTION</span></span>
<span data-ttu-id="adc62-112">列出現有的 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="adc62-113">應用程式查找可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 完成。</span><span class="sxs-lookup"><span data-stu-id="adc62-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="adc62-114">如果沒有提供參數，它會在租使用者下抓取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="adc62-115">例子</span><span class="sxs-lookup"><span data-stu-id="adc62-115">EXAMPLES</span></span>

### <span data-ttu-id="adc62-116">範例 1 - 列出所有應用程式</span><span class="sxs-lookup"><span data-stu-id="adc62-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="adc62-117">列出租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="adc62-118">範例 2 - 使用分頁功能列出應用程式</span><span class="sxs-lookup"><span data-stu-id="adc62-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="adc62-119">列出租使用者下前 100 個應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="adc62-120">範例 3 - 根據識別碼 URI 取得應用程式</span><span class="sxs-lookup"><span data-stu-id="adc62-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="adc62-121">將識別碼為 uri 的應用程式當做 http://mySecretApp1 ""。</span><span class="sxs-lookup"><span data-stu-id="adc62-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="adc62-122">範例 4 - 根據物件識別碼取得應用程式</span><span class="sxs-lookup"><span data-stu-id="adc62-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="adc62-123">使用物件識別碼為 '39e64ec6-569b-4030-8e1c-c3c519a05d69'的應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="adc62-124">參數</span><span class="sxs-lookup"><span data-stu-id="adc62-124">PARAMETERS</span></span>

### <span data-ttu-id="adc62-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="adc62-125">-ApplicationId</span></span>
<span data-ttu-id="adc62-126">要抓取的應用程式之應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc62-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc62-127">-DefaultProfile</span></span>
<span data-ttu-id="adc62-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="adc62-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adc62-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="adc62-129">-DisplayName</span></span>
<span data-ttu-id="adc62-130">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="adc62-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="adc62-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="adc62-132">從顯示名稱開始抓取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="adc62-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="adc62-133">-IdentifierUri</span></span>
<span data-ttu-id="adc62-134">要抓取之應用程式的唯一識別碼 Uri。</span><span class="sxs-lookup"><span data-stu-id="adc62-134">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="adc62-135">-ObjectId</span></span>
<span data-ttu-id="adc62-136">要抓取之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="adc62-136">The object id of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="adc62-137">-IncludeTotalCount</span></span>
<span data-ttu-id="adc62-138">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="adc62-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="adc62-139">目前，此參數沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="adc62-139">Currently, this parameter does nothing.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-140">-略過</span><span class="sxs-lookup"><span data-stu-id="adc62-140">-Skip</span></span>
<span data-ttu-id="adc62-141">忽略前 N 個物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="adc62-141">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-142">-第一個</span><span class="sxs-lookup"><span data-stu-id="adc62-142">-First</span></span>
<span data-ttu-id="adc62-143">要返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="adc62-143">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc62-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc62-144">CommonParameters</span></span>
<span data-ttu-id="adc62-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="adc62-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc62-146">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="adc62-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc62-147">輸入</span><span class="sxs-lookup"><span data-stu-id="adc62-147">INPUTS</span></span>

### <span data-ttu-id="adc62-148">System.String</span><span class="sxs-lookup"><span data-stu-id="adc62-148">System.String</span></span>

### <span data-ttu-id="adc62-149">System.Guid</span><span class="sxs-lookup"><span data-stu-id="adc62-149">System.Guid</span></span>

## <span data-ttu-id="adc62-150">輸出</span><span class="sxs-lookup"><span data-stu-id="adc62-150">OUTPUTS</span></span>

### <span data-ttu-id="adc62-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="adc62-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="adc62-152">筆記</span><span class="sxs-lookup"><span data-stu-id="adc62-152">NOTES</span></span>

## <span data-ttu-id="adc62-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="adc62-153">RELATED LINKS</span></span>

[<span data-ttu-id="adc62-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="adc62-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="adc62-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="adc62-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="adc62-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="adc62-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="adc62-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="adc62-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)


[<span data-ttu-id="adc62-158">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="adc62-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

