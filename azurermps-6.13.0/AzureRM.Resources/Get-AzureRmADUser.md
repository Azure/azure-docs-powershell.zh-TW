---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: b19571025aeb6349277e9ae366146774862e8a80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624031"
---
# <span data-ttu-id="759f9-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="759f9-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="759f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="759f9-102">SYNOPSIS</span></span>
<span data-ttu-id="759f9-103">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="759f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="759f9-104">SYNTAX</span></span>

### <span data-ttu-id="759f9-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="759f9-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="759f9-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f9-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="759f9-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f9-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="759f9-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f9-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="759f9-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f9-109">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="759f9-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="759f9-110">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="759f9-111">說明</span><span class="sxs-lookup"><span data-stu-id="759f9-111">DESCRIPTION</span></span>
<span data-ttu-id="759f9-112">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-112">Filters active directory users.</span></span>

## <span data-ttu-id="759f9-113">示例</span><span class="sxs-lookup"><span data-stu-id="759f9-113">EXAMPLES</span></span>

### <span data-ttu-id="759f9-114">範例 1-列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="759f9-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="759f9-115">列出租使用者中的所有 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="759f9-116">範例 2-使用分頁列出所有使用者</span><span class="sxs-lookup"><span data-stu-id="759f9-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzureRmADUser -First 100
```

<span data-ttu-id="759f9-117">列出租使用者中的第一個 100 AD 使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="759f9-118">範例 3-依使用者主要名稱取得 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="759f9-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="759f9-119">取得使用者主體名稱 "" 的 AD 使用者 foo@domain.com 。</span><span class="sxs-lookup"><span data-stu-id="759f9-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="759f9-120">範例 4-依搜尋字串列出</span><span class="sxs-lookup"><span data-stu-id="759f9-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="759f9-121">列出顯示名稱以「Joe」開頭的所有廣告使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="759f9-122">參數</span><span class="sxs-lookup"><span data-stu-id="759f9-122">PARAMETERS</span></span>

### <span data-ttu-id="759f9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="759f9-123">-DefaultProfile</span></span>
<span data-ttu-id="759f9-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="759f9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="759f9-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="759f9-125">-DisplayName</span></span>
<span data-ttu-id="759f9-126">使用者的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="759f9-126">The display name of the user.</span></span>

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

### <span data-ttu-id="759f9-127">-優先</span><span class="sxs-lookup"><span data-stu-id="759f9-127">-First</span></span>
<span data-ttu-id="759f9-128">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="759f9-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="759f9-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="759f9-129">-IncludeTotalCount</span></span>
<span data-ttu-id="759f9-130">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="759f9-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="759f9-131">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="759f9-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="759f9-132">-郵件</span><span class="sxs-lookup"><span data-stu-id="759f9-132">-Mail</span></span>
<span data-ttu-id="759f9-133">[使用者郵件]。</span><span class="sxs-lookup"><span data-stu-id="759f9-133">The user mail.</span></span>

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

### <span data-ttu-id="759f9-134">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="759f9-134">-ObjectId</span></span>
<span data-ttu-id="759f9-135">使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="759f9-135">Object id of the user.</span></span>

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

### <span data-ttu-id="759f9-136">-略過</span><span class="sxs-lookup"><span data-stu-id="759f9-136">-Skip</span></span>
<span data-ttu-id="759f9-137">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="759f9-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="759f9-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="759f9-138">-StartsWith</span></span>
<span data-ttu-id="759f9-139">用來尋找以所提供字串開頭的使用者。</span><span class="sxs-lookup"><span data-stu-id="759f9-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="759f9-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="759f9-140">-UserPrincipalName</span></span>
<span data-ttu-id="759f9-141">使用者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="759f9-141">UPN of the user.</span></span>

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

### <span data-ttu-id="759f9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="759f9-142">CommonParameters</span></span>
<span data-ttu-id="759f9-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="759f9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="759f9-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="759f9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="759f9-145">輸入</span><span class="sxs-lookup"><span data-stu-id="759f9-145">INPUTS</span></span>

### <span data-ttu-id="759f9-146">System.object</span><span class="sxs-lookup"><span data-stu-id="759f9-146">System.String</span></span>

### <span data-ttu-id="759f9-147">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="759f9-147">System.Guid</span></span>

## <span data-ttu-id="759f9-148">輸出</span><span class="sxs-lookup"><span data-stu-id="759f9-148">OUTPUTS</span></span>

### <span data-ttu-id="759f9-149">Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser</span><span class="sxs-lookup"><span data-stu-id="759f9-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="759f9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="759f9-150">NOTES</span></span>

## <span data-ttu-id="759f9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="759f9-151">RELATED LINKS</span></span>

[<span data-ttu-id="759f9-152">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="759f9-152">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="759f9-153">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="759f9-153">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="759f9-154">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="759f9-154">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

