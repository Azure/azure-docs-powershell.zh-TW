---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 659c2a026099eaa8764030b86a40d9ca6d4d2333
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904349"
---
# <span data-ttu-id="50e8d-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50e8d-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="50e8d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="50e8d-103">篩選 Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="50e8d-104">語法</span><span class="sxs-lookup"><span data-stu-id="50e8d-104">SYNTAX</span></span>

### <span data-ttu-id="50e8d-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50e8d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-109">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="50e8d-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e8d-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="50e8d-112">描述</span><span class="sxs-lookup"><span data-stu-id="50e8d-112">DESCRIPTION</span></span>
<span data-ttu-id="50e8d-113">篩選 Active Directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="50e8d-114">例子</span><span class="sxs-lookup"><span data-stu-id="50e8d-114">EXAMPLES</span></span>

### <span data-ttu-id="50e8d-115">範例 1：列出 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="50e8d-115">Example 1: List AD service principals</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="50e8d-116">列出租使用者中所有的 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="50e8d-117">範例 2：使用 paging 列出 AD 服務主體</span><span class="sxs-lookup"><span data-stu-id="50e8d-117">Example 2: List AD service principals using paging</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="50e8d-118">列出租使用者中前 100 個 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="50e8d-119">範例 3：按 SPN 列出服務主體</span><span class="sxs-lookup"><span data-stu-id="50e8d-119">Example 3: List service principals by SPN</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="50e8d-120">使用 SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'列出服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="50e8d-121">範例 4：按搜尋字串列出服務主體</span><span class="sxs-lookup"><span data-stu-id="50e8d-121">Example 4: List service principals by search string</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="50e8d-122">列出其顯示名稱以 「Web」為名字的所有 AD 服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="50e8d-123">範例 5：以管道列出服務主體</span><span class="sxs-lookup"><span data-stu-id="50e8d-123">Example 5: List service principals by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="50e8d-124">使用物件識別碼為 '39e64ec6-569b-4030-8e1c-c3c519a05d69' 的 AD 應用程式，並管道到 Get-AzADServicePrincipal Cmdlet，以列出該應用程式的所有服務主體。</span><span class="sxs-lookup"><span data-stu-id="50e8d-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="50e8d-125">參數</span><span class="sxs-lookup"><span data-stu-id="50e8d-125">PARAMETERS</span></span>

### <span data-ttu-id="50e8d-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50e8d-126">-ApplicationId</span></span>
<span data-ttu-id="50e8d-127">服務主體應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="50e8d-127">The service principal application id.</span></span>

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

### <span data-ttu-id="50e8d-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="50e8d-128">-ApplicationObject</span></span>
<span data-ttu-id="50e8d-129">正在取回其服務主體的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="50e8d-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50e8d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e8d-130">-DefaultProfile</span></span>
<span data-ttu-id="50e8d-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="50e8d-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50e8d-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50e8d-132">-DisplayName</span></span>
<span data-ttu-id="50e8d-133">服務主體顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="50e8d-133">The service principal display name.</span></span>

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

### <span data-ttu-id="50e8d-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="50e8d-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="50e8d-135">服務主體搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="50e8d-135">The service principal search string.</span></span>

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

### <span data-ttu-id="50e8d-136">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="50e8d-136">-ObjectId</span></span>
<span data-ttu-id="50e8d-137">服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="50e8d-137">Object id of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50e8d-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="50e8d-138">-ServicePrincipalName</span></span>
<span data-ttu-id="50e8d-139">服務的 SPN。</span><span class="sxs-lookup"><span data-stu-id="50e8d-139">SPN of the service.</span></span>

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

### <span data-ttu-id="50e8d-140">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="50e8d-140">-IncludeTotalCount</span></span>
<span data-ttu-id="50e8d-141">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="50e8d-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="50e8d-142">目前，此參數沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="50e8d-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="50e8d-143">-略過</span><span class="sxs-lookup"><span data-stu-id="50e8d-143">-Skip</span></span>
<span data-ttu-id="50e8d-144">忽略前 N 個物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="50e8d-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="50e8d-145">-第一個</span><span class="sxs-lookup"><span data-stu-id="50e8d-145">-First</span></span>
<span data-ttu-id="50e8d-146">要返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="50e8d-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="50e8d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e8d-147">CommonParameters</span></span>
<span data-ttu-id="50e8d-148">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50e8d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e8d-149">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50e8d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e8d-150">輸入</span><span class="sxs-lookup"><span data-stu-id="50e8d-150">INPUTS</span></span>

### <span data-ttu-id="50e8d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="50e8d-151">System.String</span></span>

### <span data-ttu-id="50e8d-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="50e8d-152">System.Guid</span></span>

### <span data-ttu-id="50e8d-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="50e8d-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="50e8d-154">輸出</span><span class="sxs-lookup"><span data-stu-id="50e8d-154">OUTPUTS</span></span>

### <span data-ttu-id="50e8d-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50e8d-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="50e8d-156">筆記</span><span class="sxs-lookup"><span data-stu-id="50e8d-156">NOTES</span></span>

## <span data-ttu-id="50e8d-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="50e8d-157">RELATED LINKS</span></span>

[<span data-ttu-id="50e8d-158">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50e8d-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="50e8d-159">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50e8d-159">Update-AzADServicePrincipal</span></span>](./Update-AzADServicePrincipal.md)

[<span data-ttu-id="50e8d-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="50e8d-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="50e8d-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="50e8d-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="50e8d-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="50e8d-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

