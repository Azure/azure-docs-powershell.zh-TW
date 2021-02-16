---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 68344fcafa16187651615c95ec2fb41d0bbbfb82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100128470"
---
# <span data-ttu-id="8f76c-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f76c-101">Get-AzADApplication</span></span>

## <span data-ttu-id="8f76c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8f76c-102">SYNOPSIS</span></span>
<span data-ttu-id="8f76c-103">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="8f76c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8f76c-104">SYNTAX</span></span>

### <span data-ttu-id="8f76c-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8f76c-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8f76c-106">ApplicationObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f76c-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8f76c-107">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f76c-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8f76c-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f76c-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8f76c-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f76c-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8f76c-110">ApplicationIdentifierUriParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f76c-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="8f76c-111">說明</span><span class="sxs-lookup"><span data-stu-id="8f76c-111">DESCRIPTION</span></span>
<span data-ttu-id="8f76c-112">列出現有的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="8f76c-113">應用程式查閱可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 來完成。</span><span class="sxs-lookup"><span data-stu-id="8f76c-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="8f76c-114">如果未提供任何參數，則它會提取租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="8f76c-115">示例</span><span class="sxs-lookup"><span data-stu-id="8f76c-115">EXAMPLES</span></span>

### <span data-ttu-id="8f76c-116">範例 1-列出所有應用程式</span><span class="sxs-lookup"><span data-stu-id="8f76c-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="8f76c-117">列出租使用者下的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="8f76c-118">範例 2-使用分頁的清單應用程式</span><span class="sxs-lookup"><span data-stu-id="8f76c-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="8f76c-119">列出租使用者底下的第一個100應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="8f76c-120">範例 3-透過識別碼 URI 取得應用程式</span><span class="sxs-lookup"><span data-stu-id="8f76c-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="8f76c-121">取得識別碼 uri 為 "" 的應用程式 http://mySecretApp1 。</span><span class="sxs-lookup"><span data-stu-id="8f76c-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="8f76c-122">範例 4-依物件識別碼取得應用程式</span><span class="sxs-lookup"><span data-stu-id="8f76c-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="8f76c-123">取得物件 id 為 ' 39e64ec6-569b-4030-8e1c-c3c519a05d69」的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="8f76c-124">參數</span><span class="sxs-lookup"><span data-stu-id="8f76c-124">PARAMETERS</span></span>

### <span data-ttu-id="8f76c-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8f76c-125">-ApplicationId</span></span>
<span data-ttu-id="8f76c-126">要提取之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f76c-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="8f76c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f76c-127">-DefaultProfile</span></span>
<span data-ttu-id="8f76c-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8f76c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f76c-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8f76c-129">-DisplayName</span></span>
<span data-ttu-id="8f76c-130">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8f76c-130">The display name of the application.</span></span>

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

### <span data-ttu-id="8f76c-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="8f76c-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="8f76c-132">從顯示名稱開始提取所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="8f76c-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="8f76c-133">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="8f76c-133">-IdentifierUri</span></span>
<span data-ttu-id="8f76c-134">要提取之應用程式的唯一識別碼 Uri。</span><span class="sxs-lookup"><span data-stu-id="8f76c-134">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="8f76c-135">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8f76c-135">-ObjectId</span></span>
<span data-ttu-id="8f76c-136">要提取之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f76c-136">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="8f76c-137">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="8f76c-137">-IncludeTotalCount</span></span>
<span data-ttu-id="8f76c-138">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="8f76c-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="8f76c-139">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="8f76c-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="8f76c-140">-略過</span><span class="sxs-lookup"><span data-stu-id="8f76c-140">-Skip</span></span>
<span data-ttu-id="8f76c-141">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="8f76c-141">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="8f76c-142">-優先</span><span class="sxs-lookup"><span data-stu-id="8f76c-142">-First</span></span>
<span data-ttu-id="8f76c-143">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="8f76c-143">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="8f76c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f76c-144">CommonParameters</span></span>
<span data-ttu-id="8f76c-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8f76c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f76c-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8f76c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f76c-147">輸入</span><span class="sxs-lookup"><span data-stu-id="8f76c-147">INPUTS</span></span>

### <span data-ttu-id="8f76c-148">System.object</span><span class="sxs-lookup"><span data-stu-id="8f76c-148">System.String</span></span>

### <span data-ttu-id="8f76c-149">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="8f76c-149">System.Guid</span></span>

## <span data-ttu-id="8f76c-150">輸出</span><span class="sxs-lookup"><span data-stu-id="8f76c-150">OUTPUTS</span></span>

### <span data-ttu-id="8f76c-151">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8f76c-151">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8f76c-152">筆記</span><span class="sxs-lookup"><span data-stu-id="8f76c-152">NOTES</span></span>

## <span data-ttu-id="8f76c-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="8f76c-153">RELATED LINKS</span></span>

[<span data-ttu-id="8f76c-154">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8f76c-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="8f76c-155">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8f76c-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8f76c-156">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8f76c-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8f76c-157">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f76c-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8f76c-158">新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f76c-158">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="8f76c-159">更新-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8f76c-159">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

