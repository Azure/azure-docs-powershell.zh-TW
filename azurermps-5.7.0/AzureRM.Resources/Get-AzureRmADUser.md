---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624682"
---
# <span data-ttu-id="5f0a7-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5f0a7-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="5f0a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5f0a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0a7-103">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f0a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5f0a7-104">SYNTAX</span></span>

### <span data-ttu-id="5f0a7-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5f0a7-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0a7-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0a7-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0a7-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0a7-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0a7-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0a7-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f0a7-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f0a7-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f0a7-110">說明</span><span class="sxs-lookup"><span data-stu-id="5f0a7-110">DESCRIPTION</span></span>
<span data-ttu-id="5f0a7-111">篩選 active directory 使用者。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-111">Filters active directory users.</span></span>

## <span data-ttu-id="5f0a7-112">示例</span><span class="sxs-lookup"><span data-stu-id="5f0a7-112">EXAMPLES</span></span>

### <span data-ttu-id="5f0a7-113">使用 UPN 篩選使用者</span><span class="sxs-lookup"><span data-stu-id="5f0a7-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="5f0a7-114">取得使用者的 foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="5f0a7-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="5f0a7-115">使用搜尋字串篩選使用者</span><span class="sxs-lookup"><span data-stu-id="5f0a7-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="5f0a7-116">篩選顯示名稱中含有李先生的所有 ad 使用者。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="5f0a7-117">清單廣告使用者</span><span class="sxs-lookup"><span data-stu-id="5f0a7-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="5f0a7-118">取得所有 AD 使用者</span><span class="sxs-lookup"><span data-stu-id="5f0a7-118">Gets all AD users</span></span>

## <span data-ttu-id="5f0a7-119">參數</span><span class="sxs-lookup"><span data-stu-id="5f0a7-119">PARAMETERS</span></span>

### <span data-ttu-id="5f0a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0a7-120">-DefaultProfile</span></span>
<span data-ttu-id="5f0a7-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5f0a7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0a7-122">-郵件</span><span class="sxs-lookup"><span data-stu-id="5f0a7-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0a7-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5f0a7-123">-ObjectId</span></span>
<span data-ttu-id="5f0a7-124">使用者的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0a7-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="5f0a7-125">-SearchString</span></span>
<span data-ttu-id="5f0a7-126">使用者顯示名稱</span><span class="sxs-lookup"><span data-stu-id="5f0a7-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0a7-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5f0a7-127">-UserPrincipalName</span></span>
<span data-ttu-id="5f0a7-128">使用者的 UPN。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0a7-129">CommonParameters</span></span>
<span data-ttu-id="5f0a7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0a7-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0a7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5f0a7-132">INPUTS</span></span>

### <span data-ttu-id="5f0a7-133">所有</span><span class="sxs-lookup"><span data-stu-id="5f0a7-133">None</span></span>
<span data-ttu-id="5f0a7-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5f0a7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f0a7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5f0a7-135">OUTPUTS</span></span>

### <span data-ttu-id="5f0a7-136">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADUser]</span><span class="sxs-lookup"><span data-stu-id="5f0a7-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="5f0a7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="5f0a7-137">NOTES</span></span>

## <span data-ttu-id="5f0a7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="5f0a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="5f0a7-139">新-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5f0a7-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="5f0a7-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5f0a7-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="5f0a7-141">移除-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5f0a7-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

