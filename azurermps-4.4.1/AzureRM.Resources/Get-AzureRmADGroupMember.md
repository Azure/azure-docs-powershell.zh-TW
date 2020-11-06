---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroupMember.md
ms.openlocfilehash: 17d7f922f5af46aa99e3b01aa0c0f63df05effe7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448003"
---
# <span data-ttu-id="981ad-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="981ad-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="981ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="981ad-102">SYNOPSIS</span></span>
<span data-ttu-id="981ad-103">取得群組成員。</span><span class="sxs-lookup"><span data-stu-id="981ad-103">Get a group members.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="981ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="981ad-104">SYNTAX</span></span>

```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="981ad-105">說明</span><span class="sxs-lookup"><span data-stu-id="981ad-105">DESCRIPTION</span></span>
<span data-ttu-id="981ad-106">取得群組成員。</span><span class="sxs-lookup"><span data-stu-id="981ad-106">Get a group members.</span></span>

## <span data-ttu-id="981ad-107">示例</span><span class="sxs-lookup"><span data-stu-id="981ad-107">EXAMPLES</span></span>

### <span data-ttu-id="981ad-108">--------------------------使用群組物件識別碼來篩選群組成員--------------------------</span><span class="sxs-lookup"><span data-stu-id="981ad-108">--------------------------  Filters group members using group object id  --------------------------</span></span>
```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="981ad-109">取得含有85F89C90-780E-4AA6-9F4F-6F268D322EEE 識別碼的群組成員</span><span class="sxs-lookup"><span data-stu-id="981ad-109">Gets group members with 85F89C90-780E-4AA6-9F4F-6F268D322EEE id</span></span>

## <span data-ttu-id="981ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="981ad-110">PARAMETERS</span></span>

### <span data-ttu-id="981ad-111">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="981ad-111">-GroupObjectId</span></span>
<span data-ttu-id="981ad-112">群組的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="981ad-112">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="981ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981ad-113">-DefaultProfile</span></span>
<span data-ttu-id="981ad-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="981ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="981ad-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981ad-115">CommonParameters</span></span>
<span data-ttu-id="981ad-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="981ad-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981ad-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="981ad-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981ad-118">輸入</span><span class="sxs-lookup"><span data-stu-id="981ad-118">INPUTS</span></span>

## <span data-ttu-id="981ad-119">輸出</span><span class="sxs-lookup"><span data-stu-id="981ad-119">OUTPUTS</span></span>

### <span data-ttu-id="981ad-120">[System.object]。清單 ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6 PSADObject]</span><span class="sxs-lookup"><span data-stu-id="981ad-120">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject]</span></span>

## <span data-ttu-id="981ad-121">筆記</span><span class="sxs-lookup"><span data-stu-id="981ad-121">NOTES</span></span>

## <span data-ttu-id="981ad-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="981ad-122">RELATED LINKS</span></span>

[<span data-ttu-id="981ad-123">AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="981ad-123">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="981ad-124">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="981ad-124">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

