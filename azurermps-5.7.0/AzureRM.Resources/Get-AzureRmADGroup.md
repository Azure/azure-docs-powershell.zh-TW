---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 29c3a76817bd50a5f86ea051b6de1139980a0dba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453079"
---
# <span data-ttu-id="2d065-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="2d065-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="2d065-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2d065-102">SYNOPSIS</span></span>
<span data-ttu-id="2d065-103">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="2d065-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d065-104">句法</span><span class="sxs-lookup"><span data-stu-id="2d065-104">SYNTAX</span></span>

### <span data-ttu-id="2d065-105">EmptyParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2d065-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d065-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d065-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d065-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d065-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d065-108">說明</span><span class="sxs-lookup"><span data-stu-id="2d065-108">DESCRIPTION</span></span>
<span data-ttu-id="2d065-109">篩選 active directory 群組。</span><span class="sxs-lookup"><span data-stu-id="2d065-109">Filters active directory groups.</span></span>

## <span data-ttu-id="2d065-110">示例</span><span class="sxs-lookup"><span data-stu-id="2d065-110">EXAMPLES</span></span>

### <span data-ttu-id="2d065-111">使用物件識別碼篩選群組</span><span class="sxs-lookup"><span data-stu-id="2d065-111">Filters groups using object id</span></span>
```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="2d065-112">取得含有85F89C90-780E-4AA6-9F4F-6F268D322EEE 識別碼的群組</span><span class="sxs-lookup"><span data-stu-id="2d065-112">Gets group with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

### <span data-ttu-id="2d065-113">使用搜尋字串篩選群組</span><span class="sxs-lookup"><span data-stu-id="2d065-113">Filters groups using Search String</span></span>
```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="2d065-114">篩選顯示名稱中含有 Joe 的所有廣告群組。</span><span class="sxs-lookup"><span data-stu-id="2d065-114">Filters all ad groups that has Joe in the display name.</span></span>

### <span data-ttu-id="2d065-115">清單廣告群組</span><span class="sxs-lookup"><span data-stu-id="2d065-115">List AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="2d065-116">取得所有廣告群組</span><span class="sxs-lookup"><span data-stu-id="2d065-116">Gets all AD groups</span></span>

## <span data-ttu-id="2d065-117">參數</span><span class="sxs-lookup"><span data-stu-id="2d065-117">PARAMETERS</span></span>

### <span data-ttu-id="2d065-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d065-118">-DefaultProfile</span></span>
<span data-ttu-id="2d065-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2d065-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d065-120">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2d065-120">-ObjectId</span></span>
<span data-ttu-id="2d065-121">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="2d065-121">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="2d065-122">-SearchString</span><span class="sxs-lookup"><span data-stu-id="2d065-122">-SearchString</span></span>
<span data-ttu-id="2d065-123">群組顯示名稱</span><span class="sxs-lookup"><span data-stu-id="2d065-123">The group display name</span></span>

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

### <span data-ttu-id="2d065-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d065-124">CommonParameters</span></span>
<span data-ttu-id="2d065-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2d065-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d065-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2d065-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d065-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2d065-127">INPUTS</span></span>

### <span data-ttu-id="2d065-128">所有</span><span class="sxs-lookup"><span data-stu-id="2d065-128">None</span></span>
<span data-ttu-id="2d065-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2d065-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2d065-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2d065-130">OUTPUTS</span></span>

### <span data-ttu-id="2d065-131">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADGroup]</span><span class="sxs-lookup"><span data-stu-id="2d065-131">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup]</span></span>

## <span data-ttu-id="2d065-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2d065-132">NOTES</span></span>

## <span data-ttu-id="2d065-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d065-133">RELATED LINKS</span></span>

[<span data-ttu-id="2d065-134">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="2d065-134">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="2d065-135">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2d065-135">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="2d065-136">AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="2d065-136">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

