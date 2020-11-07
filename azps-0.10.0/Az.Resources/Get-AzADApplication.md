---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 5f019f413e7ae0efa2013412499fcf34bd94a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795348"
---
# <span data-ttu-id="52da5-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="52da5-101">Get-AzADApplication</span></span>

## <span data-ttu-id="52da5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52da5-102">SYNOPSIS</span></span>
<span data-ttu-id="52da5-103">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="52da5-104">句法</span><span class="sxs-lookup"><span data-stu-id="52da5-104">SYNTAX</span></span>

### <span data-ttu-id="52da5-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="52da5-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52da5-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52da5-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52da5-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="52da5-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52da5-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="52da5-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52da5-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52da5-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52da5-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="52da5-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="52da5-111">說明</span><span class="sxs-lookup"><span data-stu-id="52da5-111">DESCRIPTION</span></span>
<span data-ttu-id="52da5-112">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="52da5-113">應用程式查閱可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 來完成。</span><span class="sxs-lookup"><span data-stu-id="52da5-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="52da5-114">如果未提供任何參數，則它會提取租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="52da5-115">示例</span><span class="sxs-lookup"><span data-stu-id="52da5-115">EXAMPLES</span></span>

### <span data-ttu-id="52da5-116">範例 1-列出所有應用程式</span><span class="sxs-lookup"><span data-stu-id="52da5-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="52da5-117">列出租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="52da5-118">範例 2-使用分頁的清單應用程式</span><span class="sxs-lookup"><span data-stu-id="52da5-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="52da5-119">列出租使用者底下的第一個100應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="52da5-120">範例 3-透過識別碼 URI 取得應用程式</span><span class="sxs-lookup"><span data-stu-id="52da5-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="52da5-121">取得識別碼 uri 為 "" 的應用程式 http://mySecretApp1 。</span><span class="sxs-lookup"><span data-stu-id="52da5-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="52da5-122">範例 4-依物件識別碼取得應用程式</span><span class="sxs-lookup"><span data-stu-id="52da5-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="52da5-123">取得物件 id 為 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="52da5-124">參數</span><span class="sxs-lookup"><span data-stu-id="52da5-124">PARAMETERS</span></span>

### <span data-ttu-id="52da5-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="52da5-125">-ApplicationId</span></span>
<span data-ttu-id="52da5-126">要提取之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="52da5-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="52da5-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52da5-127">-DefaultProfile</span></span>
<span data-ttu-id="52da5-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="52da5-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52da5-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52da5-129">-DisplayName</span></span>
<span data-ttu-id="52da5-130">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="52da5-130">The display name of the application.</span></span>

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

### <span data-ttu-id="52da5-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="52da5-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="52da5-132">從顯示名稱開始提取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="52da5-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="52da5-133">-優先</span><span class="sxs-lookup"><span data-stu-id="52da5-133">-First</span></span>
<span data-ttu-id="52da5-134">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="52da5-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="52da5-135">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="52da5-135">-IdentifierUri</span></span>
<span data-ttu-id="52da5-136">要提取之應用程式的唯一識別碼 Uri。</span><span class="sxs-lookup"><span data-stu-id="52da5-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="52da5-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="52da5-137">-IncludeTotalCount</span></span>
<span data-ttu-id="52da5-138">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="52da5-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="52da5-139">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="52da5-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="52da5-140">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="52da5-140">-ObjectId</span></span>
<span data-ttu-id="52da5-141">要提取之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="52da5-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52da5-142">-略過</span><span class="sxs-lookup"><span data-stu-id="52da5-142">-Skip</span></span>
<span data-ttu-id="52da5-143">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="52da5-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="52da5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52da5-144">CommonParameters</span></span>
<span data-ttu-id="52da5-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52da5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52da5-146">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52da5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52da5-147">輸入</span><span class="sxs-lookup"><span data-stu-id="52da5-147">INPUTS</span></span>

### <span data-ttu-id="52da5-148">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="52da5-148">System.Guid</span></span>

### <span data-ttu-id="52da5-149">System.object</span><span class="sxs-lookup"><span data-stu-id="52da5-149">System.String</span></span>

## <span data-ttu-id="52da5-150">輸出</span><span class="sxs-lookup"><span data-stu-id="52da5-150">OUTPUTS</span></span>

### <span data-ttu-id="52da5-151">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="52da5-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="52da5-152">筆記</span><span class="sxs-lookup"><span data-stu-id="52da5-152">NOTES</span></span>

## <span data-ttu-id="52da5-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="52da5-153">RELATED LINKS</span></span>

[<span data-ttu-id="52da5-154">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="52da5-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="52da5-155">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="52da5-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="52da5-156">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="52da5-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="52da5-157">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="52da5-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="52da5-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="52da5-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="52da5-159">新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="52da5-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

