---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448940"
---
# <span data-ttu-id="4125e-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="4125e-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="4125e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4125e-102">SYNOPSIS</span></span>
<span data-ttu-id="4125e-103">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4125e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4125e-104">SYNTAX</span></span>

### <span data-ttu-id="4125e-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4125e-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4125e-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="4125e-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4125e-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4125e-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="4125e-108">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4125e-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="4125e-109">說明</span><span class="sxs-lookup"><span data-stu-id="4125e-109">DESCRIPTION</span></span>
<span data-ttu-id="4125e-110">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-110">Filters active directory groups.</span></span>

## <span data-ttu-id="4125e-111">示例</span><span class="sxs-lookup"><span data-stu-id="4125e-111">EXAMPLES</span></span>

### <span data-ttu-id="4125e-112">範例 1-列出所有廣告群組</span><span class="sxs-lookup"><span data-stu-id="4125e-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="4125e-113">列出租使用者中的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="4125e-114">範例 2-使用分頁列出所有廣告群組</span><span class="sxs-lookup"><span data-stu-id="4125e-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="4125e-115">列出租使用者中的第一個 100 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="4125e-116">範例 3-依物件識別碼取得 AD 群組</span><span class="sxs-lookup"><span data-stu-id="4125e-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="4125e-117">取得物件 id 為 "85F89C90-780E-4AA6-9F4F-6F268D322EEE" 的 AD 群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="4125e-118">範例 4-依搜尋字串列出群組群組</span><span class="sxs-lookup"><span data-stu-id="4125e-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="4125e-119">列出顯示名稱以「Joe」開頭的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="4125e-120">參數</span><span class="sxs-lookup"><span data-stu-id="4125e-120">PARAMETERS</span></span>

### <span data-ttu-id="4125e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4125e-121">-DefaultProfile</span></span>
<span data-ttu-id="4125e-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4125e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4125e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4125e-123">-DisplayName</span></span>
<span data-ttu-id="4125e-124">群組的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="4125e-124">The display name of the group.</span></span>

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

### <span data-ttu-id="4125e-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="4125e-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="4125e-126">用來尋找以所提供字串開頭的群組。</span><span class="sxs-lookup"><span data-stu-id="4125e-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="4125e-127">-優先</span><span class="sxs-lookup"><span data-stu-id="4125e-127">-First</span></span>
<span data-ttu-id="4125e-128">要傳回的物件數目上限。</span><span class="sxs-lookup"><span data-stu-id="4125e-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="4125e-129">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="4125e-129">-IncludeTotalCount</span></span>
<span data-ttu-id="4125e-130">報告資料集中的物件數目。</span><span class="sxs-lookup"><span data-stu-id="4125e-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="4125e-131">這個參數目前不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="4125e-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="4125e-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4125e-132">-ObjectId</span></span>
<span data-ttu-id="4125e-133">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="4125e-133">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="4125e-134">-略過</span><span class="sxs-lookup"><span data-stu-id="4125e-134">-Skip</span></span>
<span data-ttu-id="4125e-135">忽略前 N 個物件，然後取得剩餘的物件。</span><span class="sxs-lookup"><span data-stu-id="4125e-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="4125e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4125e-136">CommonParameters</span></span>
<span data-ttu-id="4125e-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4125e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4125e-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4125e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4125e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="4125e-139">INPUTS</span></span>

### <span data-ttu-id="4125e-140">System.object</span><span class="sxs-lookup"><span data-stu-id="4125e-140">System.String</span></span>

### <span data-ttu-id="4125e-141">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="4125e-141">System.Guid</span></span>

## <span data-ttu-id="4125e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4125e-142">OUTPUTS</span></span>

### <span data-ttu-id="4125e-143">Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup</span><span class="sxs-lookup"><span data-stu-id="4125e-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="4125e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4125e-144">NOTES</span></span>

## <span data-ttu-id="4125e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="4125e-145">RELATED LINKS</span></span>

[<span data-ttu-id="4125e-146">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="4125e-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="4125e-147">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4125e-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="4125e-148">AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="4125e-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

