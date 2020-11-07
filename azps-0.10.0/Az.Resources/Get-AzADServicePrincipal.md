---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: a80e2b8603995ba57aada9639b3a6b45e08e2e55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795339"
---
# <span data-ttu-id="4291a-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4291a-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="4291a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4291a-102">SYNOPSIS</span></span>
<span data-ttu-id="4291a-103">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="4291a-104">句法</span><span class="sxs-lookup"><span data-stu-id="4291a-104">SYNTAX</span></span>

### <span data-ttu-id="4291a-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4291a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4291a-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="4291a-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4291a-112">說明</span><span class="sxs-lookup"><span data-stu-id="4291a-112">DESCRIPTION</span></span>
<span data-ttu-id="4291a-113">篩選 active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="4291a-114">示例</span><span class="sxs-lookup"><span data-stu-id="4291a-114">EXAMPLES</span></span>

### <span data-ttu-id="4291a-115">範例 1-清單廣告服務原則</span><span class="sxs-lookup"><span data-stu-id="4291a-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="4291a-116">列出租使用者中的所有廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="4291a-117">範例 2-使用分頁來列出廣告服務主體</span><span class="sxs-lookup"><span data-stu-id="4291a-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="4291a-118">列出租使用者中的第一個 100 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="4291a-119">範例3：依 SPN 列出服務主體</span><span class="sxs-lookup"><span data-stu-id="4291a-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="4291a-120">列出 SPN 為「36f81fc3-b00f-48cd-8218-3879f51ff39f」的服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="4291a-121">範例4：依搜尋字串列出服務主體</span><span class="sxs-lookup"><span data-stu-id="4291a-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="4291a-122">列出顯示名稱以 "Web" 開頭的所有廣告服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="4291a-123">範例5：依管道列出服務主體</span><span class="sxs-lookup"><span data-stu-id="4291a-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="4291a-124">取得物件 id 為 "39e64ec6-569b-4030-8e1c-c3c519a05d69" 的 AD 應用程式，並將其管道至 Get-AzADServicePrincipal Cmdlet，以列出該應用程式的所有服務主體。</span><span class="sxs-lookup"><span data-stu-id="4291a-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="4291a-125">參數</span><span class="sxs-lookup"><span data-stu-id="4291a-125">PARAMETERS</span></span>

### <span data-ttu-id="4291a-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4291a-126">-ApplicationId</span></span>
<span data-ttu-id="4291a-127">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="4291a-127">The service principal application id.</span></span>

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

### <span data-ttu-id="4291a-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="4291a-128">-ApplicationObject</span></span>
<span data-ttu-id="4291a-129">要檢索其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="4291a-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4291a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4291a-130">-DefaultProfile</span></span>
<span data-ttu-id="4291a-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4291a-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4291a-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4291a-132">-DisplayName</span></span>
<span data-ttu-id="4291a-133">服務主體顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4291a-133">The service principal display name.</span></span>

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

### <span data-ttu-id="4291a-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="4291a-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="4291a-135">服務主體搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="4291a-135">The service principal search string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4291a-136">-優先</span><span class="sxs-lookup"><span data-stu-id="4291a-136">-First</span></span>
<span data-ttu-id="4291a-137">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="4291a-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4291a-138">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4291a-138">-IncludeTotalCount</span></span>
<span data-ttu-id="4291a-139">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="4291a-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4291a-140">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="4291a-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4291a-141">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4291a-141">-ObjectId</span></span>
<span data-ttu-id="4291a-142">服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="4291a-142">Object id of the service principal.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4291a-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4291a-143">-ServicePrincipalName</span></span>
<span data-ttu-id="4291a-144">服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="4291a-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4291a-145">-略過</span><span class="sxs-lookup"><span data-stu-id="4291a-145">-Skip</span></span>
<span data-ttu-id="4291a-146">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="4291a-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4291a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4291a-147">CommonParameters</span></span>
<span data-ttu-id="4291a-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4291a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4291a-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4291a-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4291a-150">輸入</span><span class="sxs-lookup"><span data-stu-id="4291a-150">INPUTS</span></span>

### <span data-ttu-id="4291a-151">System.object</span><span class="sxs-lookup"><span data-stu-id="4291a-151">System.String</span></span>

### <span data-ttu-id="4291a-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="4291a-152">System.Guid</span></span>

### <span data-ttu-id="4291a-153">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4291a-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="4291a-154">參數： ApplicationObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4291a-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="4291a-155">輸出</span><span class="sxs-lookup"><span data-stu-id="4291a-155">OUTPUTS</span></span>

### <span data-ttu-id="4291a-156">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4291a-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="4291a-157">筆記</span><span class="sxs-lookup"><span data-stu-id="4291a-157">NOTES</span></span>

## <span data-ttu-id="4291a-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4291a-158">RELATED LINKS</span></span>

[<span data-ttu-id="4291a-159">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4291a-159">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="4291a-160">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4291a-160">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="4291a-161">移除-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4291a-161">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="4291a-162">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4291a-162">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="4291a-163">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="4291a-163">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

