---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: f2bba3b69205585cd6d8f4834803a82bf15ec305
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277259"
---
# <span data-ttu-id="db5bc-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="db5bc-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="db5bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db5bc-102">SYNOPSIS</span></span>
<span data-ttu-id="db5bc-103">為 PeerAsn 建立記憶體連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db5bc-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="db5bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="db5bc-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db5bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="db5bc-105">DESCRIPTION</span></span>
<span data-ttu-id="db5bc-106">在 [記憶體 PeerAsn] 中建立連絡人的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="db5bc-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="db5bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="db5bc-107">EXAMPLES</span></span>

### <span data-ttu-id="db5bc-108">建立連絡人詳細資料並新增至 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="db5bc-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="db5bc-109">角色和電子郵件是必要的。</span><span class="sxs-lookup"><span data-stu-id="db5bc-109">Role and email are required.</span></span> <span data-ttu-id="db5bc-110">[電話] 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="db5bc-110">Phone is optional.</span></span> <span data-ttu-id="db5bc-111">手機支援 +- ( # A1 或空格。</span><span class="sxs-lookup"><span data-stu-id="db5bc-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="db5bc-112">PeerAsn 必須包含至少一個 "Noc" 類型的連絡人詳細資料</span><span class="sxs-lookup"><span data-stu-id="db5bc-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="db5bc-113">參數</span><span class="sxs-lookup"><span data-stu-id="db5bc-113">PARAMETERS</span></span>

### <span data-ttu-id="db5bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5bc-114">-DefaultProfile</span></span>
<span data-ttu-id="db5bc-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db5bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5bc-116">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="db5bc-116">-Email</span></span>
<span data-ttu-id="db5bc-117">當問題 arrise 通常是網路運營中心時，用來聯絡的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="db5bc-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bc-118">-電話</span><span class="sxs-lookup"><span data-stu-id="db5bc-118">-Phone</span></span>
<span data-ttu-id="db5bc-119">當問題 arrise 通常是網路運營中心時，用來聯絡的電話</span><span class="sxs-lookup"><span data-stu-id="db5bc-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bc-120">-角色</span><span class="sxs-lookup"><span data-stu-id="db5bc-120">-Role</span></span>
<span data-ttu-id="db5bc-121">選擇最適合連絡人資訊的角色。</span><span class="sxs-lookup"><span data-stu-id="db5bc-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="db5bc-122">必須提供 NOC 連絡人。</span><span class="sxs-lookup"><span data-stu-id="db5bc-122">NOC Contact is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db5bc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5bc-123">CommonParameters</span></span>
<span data-ttu-id="db5bc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db5bc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5bc-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="db5bc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5bc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="db5bc-126">INPUTS</span></span>

### <span data-ttu-id="db5bc-127">所有</span><span class="sxs-lookup"><span data-stu-id="db5bc-127">None</span></span>

## <span data-ttu-id="db5bc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="db5bc-128">OUTPUTS</span></span>

### <span data-ttu-id="db5bc-129">PSContactDetail 中的 [對等]</span><span class="sxs-lookup"><span data-stu-id="db5bc-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="db5bc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="db5bc-130">NOTES</span></span>

## <span data-ttu-id="db5bc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="db5bc-131">RELATED LINKS</span></span>
