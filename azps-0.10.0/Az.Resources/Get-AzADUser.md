---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795337"
---
# <span data-ttu-id="5a405-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5a405-101">Get-AzADUser</span></span>

## <span data-ttu-id="5a405-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a405-102">SYNOPSIS</span></span>
<span data-ttu-id="5a405-103">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-103">Filters active directory users.</span></span>

## <span data-ttu-id="5a405-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a405-104">SYNTAX</span></span>

### <span data-ttu-id="5a405-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5a405-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5a405-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a405-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5a405-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a405-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5a405-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a405-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5a405-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a405-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5a405-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a405-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5a405-111">說明</span><span class="sxs-lookup"><span data-stu-id="5a405-111">DESCRIPTION</span></span>
<span data-ttu-id="5a405-112">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-112">Filters active directory users.</span></span>

## <span data-ttu-id="5a405-113">示例</span><span class="sxs-lookup"><span data-stu-id="5a405-113">EXAMPLES</span></span>

### <span data-ttu-id="5a405-114">範例 1-列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="5a405-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="5a405-115">列出租使用者中的所有 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="5a405-116">範例 2-使用分頁列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="5a405-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="5a405-117">列出租使用者中的第一個 100 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="5a405-118">範例 3-依使用者主要名稱取得 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="5a405-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="5a405-119">取得使用者主體名稱 "" 的 AD 使用者 foo@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="5a405-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="5a405-120">範例 4-依搜尋字串列出</span><span class="sxs-lookup"><span data-stu-id="5a405-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="5a405-121">列出顯示名稱以「Joe」開頭的所有廣告使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="5a405-122">參數</span><span class="sxs-lookup"><span data-stu-id="5a405-122">PARAMETERS</span></span>

### <span data-ttu-id="5a405-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a405-123">-DefaultProfile</span></span>
<span data-ttu-id="5a405-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a405-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a405-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5a405-125">-DisplayName</span></span>
<span data-ttu-id="5a405-126">使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="5a405-126">The display name of the user.</span></span>

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

### <span data-ttu-id="5a405-127">-優先</span><span class="sxs-lookup"><span data-stu-id="5a405-127">-First</span></span>
<span data-ttu-id="5a405-128">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="5a405-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="5a405-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="5a405-129">-IncludeTotalCount</span></span>
<span data-ttu-id="5a405-130">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="5a405-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5a405-131">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="5a405-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5a405-132">-郵件</span><span class="sxs-lookup"><span data-stu-id="5a405-132">-Mail</span></span>
<span data-ttu-id="5a405-133">[使用者郵件]。</span><span class="sxs-lookup"><span data-stu-id="5a405-133">The user mail.</span></span>

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

### <span data-ttu-id="5a405-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a405-134">-ObjectId</span></span>
<span data-ttu-id="5a405-135">使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a405-135">Object id of the user.</span></span>

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

### <span data-ttu-id="5a405-136">-略過</span><span class="sxs-lookup"><span data-stu-id="5a405-136">-Skip</span></span>
<span data-ttu-id="5a405-137">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="5a405-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="5a405-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="5a405-138">-StartsWith</span></span>
<span data-ttu-id="5a405-139">用來尋找以所提供字串開頭的使用者。</span><span class="sxs-lookup"><span data-stu-id="5a405-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="5a405-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5a405-140">-UserPrincipalName</span></span>
<span data-ttu-id="5a405-141">使用者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="5a405-141">UPN of the user.</span></span>

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

### <span data-ttu-id="5a405-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a405-142">CommonParameters</span></span>
<span data-ttu-id="5a405-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a405-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a405-144">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5a405-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a405-145">輸入</span><span class="sxs-lookup"><span data-stu-id="5a405-145">INPUTS</span></span>

### <span data-ttu-id="5a405-146">System.object</span><span class="sxs-lookup"><span data-stu-id="5a405-146">System.String</span></span>

### <span data-ttu-id="5a405-147">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="5a405-147">System.Guid</span></span>

## <span data-ttu-id="5a405-148">輸出</span><span class="sxs-lookup"><span data-stu-id="5a405-148">OUTPUTS</span></span>

### <span data-ttu-id="5a405-149">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="5a405-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="5a405-150">筆記</span><span class="sxs-lookup"><span data-stu-id="5a405-150">NOTES</span></span>

## <span data-ttu-id="5a405-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a405-151">RELATED LINKS</span></span>

[<span data-ttu-id="5a405-152">新-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5a405-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="5a405-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5a405-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="5a405-154">移除-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5a405-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

