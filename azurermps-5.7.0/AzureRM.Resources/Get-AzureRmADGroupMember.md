---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: c3a783178bf8342e891f8eab2996e77a2045721a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625000"
---
# <span data-ttu-id="046c5-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="046c5-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="046c5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="046c5-102">SYNOPSIS</span></span>
<span data-ttu-id="046c5-103">取得群組成員。</span><span class="sxs-lookup"><span data-stu-id="046c5-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="046c5-104">句法</span><span class="sxs-lookup"><span data-stu-id="046c5-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="046c5-105">說明</span><span class="sxs-lookup"><span data-stu-id="046c5-105">DESCRIPTION</span></span>
<span data-ttu-id="046c5-106">取得群組成員。</span><span class="sxs-lookup"><span data-stu-id="046c5-106">Get a group members.</span></span>

## <span data-ttu-id="046c5-107">示例</span><span class="sxs-lookup"><span data-stu-id="046c5-107">EXAMPLES</span></span>

### <span data-ttu-id="046c5-108">使用群組物件識別碼篩選群組成員</span><span class="sxs-lookup"><span data-stu-id="046c5-108">Filters group members using group object id</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="046c5-109">取得含有85F89C90-780E-4AA6-9F4F-6F268D322EEE 識別碼的群組成員</span><span class="sxs-lookup"><span data-stu-id="046c5-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="046c5-110">參數</span><span class="sxs-lookup"><span data-stu-id="046c5-110">PARAMETERS</span></span>

### <span data-ttu-id="046c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="046c5-111">-DefaultProfile</span></span>
<span data-ttu-id="046c5-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="046c5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="046c5-113">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="046c5-113">-GroupObjectId</span></span>
<span data-ttu-id="046c5-114">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="046c5-114">Object id of the group.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="046c5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="046c5-115">CommonParameters</span></span>
<span data-ttu-id="046c5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="046c5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="046c5-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="046c5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="046c5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="046c5-118">INPUTS</span></span>

### <span data-ttu-id="046c5-119">所有</span><span class="sxs-lookup"><span data-stu-id="046c5-119">None</span></span>
<span data-ttu-id="046c5-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="046c5-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="046c5-121">輸出</span><span class="sxs-lookup"><span data-stu-id="046c5-121">OUTPUTS</span></span>

### <span data-ttu-id="046c5-122">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADObject]</span><span class="sxs-lookup"><span data-stu-id="046c5-122">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="046c5-123">筆記</span><span class="sxs-lookup"><span data-stu-id="046c5-123">NOTES</span></span>

## <span data-ttu-id="046c5-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="046c5-124">RELATED LINKS</span></span>

[<span data-ttu-id="046c5-125">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="046c5-125">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="046c5-126">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="046c5-126">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

