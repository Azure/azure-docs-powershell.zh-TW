---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 884d5086c8966da8622d48e85f5f4b3009fcc94f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139653"
---
# <span data-ttu-id="e0ae1-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e0ae1-101">Get-AzADUser</span></span>

## <span data-ttu-id="e0ae1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0ae1-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ae1-103">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-103">Filters active directory users.</span></span>

## <span data-ttu-id="e0ae1-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0ae1-104">SYNTAX</span></span>

### <span data-ttu-id="e0ae1-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e0ae1-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0ae1-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ae1-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0ae1-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ae1-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0ae1-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ae1-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0ae1-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ae1-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e0ae1-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ae1-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e0ae1-111">說明</span><span class="sxs-lookup"><span data-stu-id="e0ae1-111">DESCRIPTION</span></span>
<span data-ttu-id="e0ae1-112">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-112">Filters active directory users.</span></span>

## <span data-ttu-id="e0ae1-113">示例</span><span class="sxs-lookup"><span data-stu-id="e0ae1-113">EXAMPLES</span></span>

### <span data-ttu-id="e0ae1-114">範例1：列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="e0ae1-114">Example 1: List all users</span></span>

```powershell
PS C:\> Get-AzADUser
```

<span data-ttu-id="e0ae1-115">列出租使用者中的所有 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="e0ae1-116">範例2：使用分頁列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="e0ae1-116">Example 2: List all users using paging</span></span>

```powershell
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="e0ae1-117">列出租使用者中的第一個 100 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="e0ae1-118">範例3：依使用者主要名稱取得 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="e0ae1-118">Example 3: Get AD user by user principal name</span></span>

```powershell
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="e0ae1-119">取得使用者主體名稱 "" 的 AD 使用者 foo@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="e0ae1-120">範例4：依搜尋字串列出清單</span><span class="sxs-lookup"><span data-stu-id="e0ae1-120">Example 4: List by search string</span></span>

```powershell
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="e0ae1-121">列出顯示名稱以「Joe」開頭的所有廣告使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="e0ae1-122">參數</span><span class="sxs-lookup"><span data-stu-id="e0ae1-122">PARAMETERS</span></span>

### <span data-ttu-id="e0ae1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ae1-123">-DefaultProfile</span></span>
<span data-ttu-id="e0ae1-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e0ae1-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0ae1-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e0ae1-125">-DisplayName</span></span>
<span data-ttu-id="e0ae1-126">使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-126">The display name of the user.</span></span>

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

### <span data-ttu-id="e0ae1-127">-郵件</span><span class="sxs-lookup"><span data-stu-id="e0ae1-127">-Mail</span></span>
<span data-ttu-id="e0ae1-128">[使用者郵件]。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-128">The user mail.</span></span>

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

### <span data-ttu-id="e0ae1-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e0ae1-129">-ObjectId</span></span>
<span data-ttu-id="e0ae1-130">使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-130">Object id of the user.</span></span>

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

### <span data-ttu-id="e0ae1-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="e0ae1-131">-StartsWith</span></span>
<span data-ttu-id="e0ae1-132">用來尋找以所提供字串開頭的使用者。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="e0ae1-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e0ae1-133">-UserPrincipalName</span></span>
<span data-ttu-id="e0ae1-134">使用者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-134">UPN of the user.</span></span>

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

### <span data-ttu-id="e0ae1-135">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="e0ae1-135">-IncludeTotalCount</span></span>
<span data-ttu-id="e0ae1-136">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e0ae1-137">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e0ae1-138">-略過</span><span class="sxs-lookup"><span data-stu-id="e0ae1-138">-Skip</span></span>
<span data-ttu-id="e0ae1-139">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e0ae1-140">-優先</span><span class="sxs-lookup"><span data-stu-id="e0ae1-140">-First</span></span>
<span data-ttu-id="e0ae1-141">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e0ae1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ae1-142">CommonParameters</span></span>
<span data-ttu-id="e0ae1-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ae1-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ae1-145">輸入</span><span class="sxs-lookup"><span data-stu-id="e0ae1-145">INPUTS</span></span>

### <span data-ttu-id="e0ae1-146">System.object</span><span class="sxs-lookup"><span data-stu-id="e0ae1-146">System.String</span></span>

## <span data-ttu-id="e0ae1-147">輸出</span><span class="sxs-lookup"><span data-stu-id="e0ae1-147">OUTPUTS</span></span>

### <span data-ttu-id="e0ae1-148">PSADUser （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="e0ae1-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="e0ae1-149">筆記</span><span class="sxs-lookup"><span data-stu-id="e0ae1-149">NOTES</span></span>

## <span data-ttu-id="e0ae1-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0ae1-150">RELATED LINKS</span></span>

[<span data-ttu-id="e0ae1-151">新-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e0ae1-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="e0ae1-152">更新-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e0ae1-152">Update-AzADUser</span></span>](./Update-AzADUser.md)

[<span data-ttu-id="e0ae1-153">移除-AzADUser</span><span class="sxs-lookup"><span data-stu-id="e0ae1-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

