---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeerasncontactdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeerAsnContactDetail.md
ms.openlocfilehash: 978c513646c08577f4fa15b8a0e460320878c7c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911466"
---
# <span data-ttu-id="6f571-101">New-AzPeerAsnContactDetail</span><span class="sxs-lookup"><span data-stu-id="6f571-101">New-AzPeerAsnContactDetail</span></span>

## <span data-ttu-id="6f571-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f571-102">SYNOPSIS</span></span>
<span data-ttu-id="6f571-103">為 PeerAsn 建立記憶體中的連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f571-103">Creates an in memory contact detail for PeerAsn.</span></span> 

## <span data-ttu-id="6f571-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f571-104">SYNTAX</span></span>

```
New-AzPeerAsnContactDetail -Role <String> -Email <String> [-Phone <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f571-105">描述</span><span class="sxs-lookup"><span data-stu-id="6f571-105">DESCRIPTION</span></span>
<span data-ttu-id="6f571-106">在記憶體中建立對等連絡人詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6f571-106">Create an in memory PeerAsn contact detail.</span></span>

## <span data-ttu-id="6f571-107">例子</span><span class="sxs-lookup"><span data-stu-id="6f571-107">EXAMPLES</span></span>

### <span data-ttu-id="6f571-108">建立連絡人詳細資料並新增到 PeerAsn</span><span class="sxs-lookup"><span data-stu-id="6f571-108">Create contact detail and add to PeerAsn</span></span>
```powershell
PS C:\> $nocContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> $customerContact = New-AzPeerAsnContactDetail -Role Noc -Email "noc@contoso.com" -Phone "+1 (887) 888-8088"
PS C:\> New-AzPeerAsn -Name $name -PeerName "Contoso Networks Limited" -PeerAsn 65000 -ContactDetail $nocContact,$customerContact
```

<span data-ttu-id="6f571-109">角色和電子郵件為必填專案。</span><span class="sxs-lookup"><span data-stu-id="6f571-109">Role and email are required.</span></span> <span data-ttu-id="6f571-110">電話是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="6f571-110">Phone is optional.</span></span> <span data-ttu-id="6f571-111">電話支援 +- () 或空格。</span><span class="sxs-lookup"><span data-stu-id="6f571-111">Phone supports +-() or spaces.</span></span> <span data-ttu-id="6f571-112">對等體必須包含至少一個類型為 "Noc" 的連絡人詳細資料</span><span class="sxs-lookup"><span data-stu-id="6f571-112">A PeerAsn must include at least one contact detail of type "Noc"</span></span>

## <span data-ttu-id="6f571-113">參數</span><span class="sxs-lookup"><span data-stu-id="6f571-113">PARAMETERS</span></span>

### <span data-ttu-id="6f571-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f571-114">-DefaultProfile</span></span>
<span data-ttu-id="6f571-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f571-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f571-116">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="6f571-116">-Email</span></span>
<span data-ttu-id="6f571-117">如果問題通常是網路營運中心，用來聯繫的電子郵件地址</span><span class="sxs-lookup"><span data-stu-id="6f571-117">Email Addresses used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="6f571-118">-電話</span><span class="sxs-lookup"><span data-stu-id="6f571-118">-Phone</span></span>
<span data-ttu-id="6f571-119">如果問題通常是網路營運中心，用來聯繫的電話</span><span class="sxs-lookup"><span data-stu-id="6f571-119">Phone used to contact if issues arrise typically a Network Operations Center</span></span>

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

### <span data-ttu-id="6f571-120">-角色</span><span class="sxs-lookup"><span data-stu-id="6f571-120">-Role</span></span>
<span data-ttu-id="6f571-121">選擇最適合連絡人資訊的角色。</span><span class="sxs-lookup"><span data-stu-id="6f571-121">Choose the role that best suits the contact information.</span></span>
<span data-ttu-id="6f571-122">NOC Contact 為必填專案。</span><span class="sxs-lookup"><span data-stu-id="6f571-122">NOC Contact is required.</span></span>

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

### <span data-ttu-id="6f571-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f571-123">CommonParameters</span></span>
<span data-ttu-id="6f571-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f571-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f571-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f571-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f571-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6f571-126">INPUTS</span></span>

### <span data-ttu-id="6f571-127">沒有</span><span class="sxs-lookup"><span data-stu-id="6f571-127">None</span></span>

## <span data-ttu-id="6f571-128">輸出</span><span class="sxs-lookup"><span data-stu-id="6f571-128">OUTPUTS</span></span>

### <span data-ttu-id="6f571-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.models.PSContactDetail</span><span class="sxs-lookup"><span data-stu-id="6f571-129">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSContactDetail</span></span>

## <span data-ttu-id="6f571-130">筆記</span><span class="sxs-lookup"><span data-stu-id="6f571-130">NOTES</span></span>

## <span data-ttu-id="6f571-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f571-131">RELATED LINKS</span></span>
