---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 6f5ae29865775368427987dcfc1844c9235db593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904345"
---
# <span data-ttu-id="b22af-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b22af-101">Get-AzADUser</span></span>

## <span data-ttu-id="b22af-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b22af-102">SYNOPSIS</span></span>
<span data-ttu-id="b22af-103">篩選 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-103">Filters active directory users.</span></span>

## <span data-ttu-id="b22af-104">語法</span><span class="sxs-lookup"><span data-stu-id="b22af-104">SYNTAX</span></span>

### <span data-ttu-id="b22af-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b22af-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b22af-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22af-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b22af-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22af-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b22af-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22af-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b22af-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22af-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="b22af-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="b22af-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="b22af-111">描述</span><span class="sxs-lookup"><span data-stu-id="b22af-111">DESCRIPTION</span></span>
<span data-ttu-id="b22af-112">篩選 Active Directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-112">Filters active directory users.</span></span>

## <span data-ttu-id="b22af-113">例子</span><span class="sxs-lookup"><span data-stu-id="b22af-113">EXAMPLES</span></span>

### <span data-ttu-id="b22af-114">範例 1：列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="b22af-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="b22af-115">列出租使用者中所有的 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="b22af-116">範例 2：列出使用分頁的所有使用者</span><span class="sxs-lookup"><span data-stu-id="b22af-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="b22af-117">列出租使用者中的前 100 個 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="b22af-118">範例 3：根據使用者主體名稱取得 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="b22af-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="b22af-119">使用使用者主體名稱 " "" 獲得 foo@domain.com AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="b22af-120">範例 4：按搜尋字串列出</span><span class="sxs-lookup"><span data-stu-id="b22af-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="b22af-121">列出顯示名稱以 "Joe" 開頭的所有 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="b22af-122">參數</span><span class="sxs-lookup"><span data-stu-id="b22af-122">PARAMETERS</span></span>

### <span data-ttu-id="b22af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b22af-123">-DefaultProfile</span></span>
<span data-ttu-id="b22af-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b22af-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b22af-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b22af-125">-DisplayName</span></span>
<span data-ttu-id="b22af-126">使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="b22af-126">The display name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b22af-127">-郵件</span><span class="sxs-lookup"><span data-stu-id="b22af-127">-Mail</span></span>
<span data-ttu-id="b22af-128">使用者郵件。</span><span class="sxs-lookup"><span data-stu-id="b22af-128">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22af-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b22af-129">-ObjectId</span></span>
<span data-ttu-id="b22af-130">使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b22af-130">Object id of the user.</span></span>

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

### <span data-ttu-id="b22af-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="b22af-131">-StartsWith</span></span>
<span data-ttu-id="b22af-132">用來尋找以所提供的字串開頭的使用者。</span><span class="sxs-lookup"><span data-stu-id="b22af-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="b22af-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b22af-133">-UserPrincipalName</span></span>
<span data-ttu-id="b22af-134">使用者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="b22af-134">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b22af-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="b22af-135">-IncludeTotalCount</span></span>
<span data-ttu-id="b22af-136">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="b22af-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="b22af-137">目前，此參數沒有任何影響。</span><span class="sxs-lookup"><span data-stu-id="b22af-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="b22af-138">-略過</span><span class="sxs-lookup"><span data-stu-id="b22af-138">-Skip</span></span>
<span data-ttu-id="b22af-139">忽略前 N 個物件，然後獲得其餘的物件。</span><span class="sxs-lookup"><span data-stu-id="b22af-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="b22af-140">-第一個</span><span class="sxs-lookup"><span data-stu-id="b22af-140">-First</span></span>
<span data-ttu-id="b22af-141">要返回的物件數量上限。</span><span class="sxs-lookup"><span data-stu-id="b22af-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="b22af-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b22af-142">CommonParameters</span></span>
<span data-ttu-id="b22af-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b22af-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b22af-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b22af-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b22af-145">輸入</span><span class="sxs-lookup"><span data-stu-id="b22af-145">INPUTS</span></span>

### <span data-ttu-id="b22af-146">System.String</span><span class="sxs-lookup"><span data-stu-id="b22af-146">System.String</span></span>

## <span data-ttu-id="b22af-147">輸出</span><span class="sxs-lookup"><span data-stu-id="b22af-147">OUTPUTS</span></span>

### <span data-ttu-id="b22af-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="b22af-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="b22af-149">筆記</span><span class="sxs-lookup"><span data-stu-id="b22af-149">NOTES</span></span>

## <span data-ttu-id="b22af-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="b22af-150">RELATED LINKS</span></span>

[<span data-ttu-id="b22af-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b22af-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="b22af-152">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b22af-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="b22af-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="b22af-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

