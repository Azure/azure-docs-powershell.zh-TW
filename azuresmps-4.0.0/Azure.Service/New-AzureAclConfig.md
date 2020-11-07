---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CD2274E5-B3D4-489E-B374-8B2BCC1F923E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90666be18ee3e546620d0c10386594b8ae7ec8a0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967681"
---
# <span data-ttu-id="133a7-101">New-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="133a7-101">New-AzureAclConfig</span></span>

## <span data-ttu-id="133a7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="133a7-102">SYNOPSIS</span></span>
<span data-ttu-id="133a7-103">建立空白的 ACL 設定物件。</span><span class="sxs-lookup"><span data-stu-id="133a7-103">Creates an empty ACL configuration object.</span></span>

## <span data-ttu-id="133a7-104">句法</span><span class="sxs-lookup"><span data-stu-id="133a7-104">SYNTAX</span></span>

```
New-AzureAclConfig [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="133a7-105">說明</span><span class="sxs-lookup"><span data-stu-id="133a7-105">DESCRIPTION</span></span>
<span data-ttu-id="133a7-106">**新的-AzureAclConfig** Cmdlet 會 (ACL) 設定物件中建立空白的存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="133a7-106">The **New-AzureAclConfig** cmdlet creates an empty access control list (ACL) configuration object.</span></span>

## <span data-ttu-id="133a7-107">示例</span><span class="sxs-lookup"><span data-stu-id="133a7-107">EXAMPLES</span></span>

### <span data-ttu-id="133a7-108">範例1：建立 ACL 設定物件</span><span class="sxs-lookup"><span data-stu-id="133a7-108">Example 1: Create an ACL configuration object</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
```

<span data-ttu-id="133a7-109">這個命令會建立一個空白的 ACL 設定物件，然後將它儲存在 $Acl 變數中。</span><span class="sxs-lookup"><span data-stu-id="133a7-109">This command creates an empty ACL configuration object, and then stores it in the $Acl variable.</span></span>

## <span data-ttu-id="133a7-110">參數</span><span class="sxs-lookup"><span data-stu-id="133a7-110">PARAMETERS</span></span>

### <span data-ttu-id="133a7-111">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="133a7-111">-InformationAction</span></span>
<span data-ttu-id="133a7-112">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="133a7-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="133a7-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="133a7-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="133a7-114">持續</span><span class="sxs-lookup"><span data-stu-id="133a7-114">Continue</span></span>
- <span data-ttu-id="133a7-115">理會</span><span class="sxs-lookup"><span data-stu-id="133a7-115">Ignore</span></span>
- <span data-ttu-id="133a7-116">看</span><span class="sxs-lookup"><span data-stu-id="133a7-116">Inquire</span></span>
- <span data-ttu-id="133a7-117">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="133a7-117">SilentlyContinue</span></span>
- <span data-ttu-id="133a7-118">停止</span><span class="sxs-lookup"><span data-stu-id="133a7-118">Stop</span></span>
- <span data-ttu-id="133a7-119">封存</span><span class="sxs-lookup"><span data-stu-id="133a7-119">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133a7-120">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="133a7-120">-InformationVariable</span></span>
<span data-ttu-id="133a7-121">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="133a7-121">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="133a7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="133a7-122">CommonParameters</span></span>
<span data-ttu-id="133a7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="133a7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="133a7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="133a7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="133a7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="133a7-125">INPUTS</span></span>

## <span data-ttu-id="133a7-126">輸出</span><span class="sxs-lookup"><span data-stu-id="133a7-126">OUTPUTS</span></span>

## <span data-ttu-id="133a7-127">筆記</span><span class="sxs-lookup"><span data-stu-id="133a7-127">NOTES</span></span>

## <span data-ttu-id="133a7-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="133a7-128">RELATED LINKS</span></span>

[<span data-ttu-id="133a7-129">AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="133a7-129">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="133a7-130">移除-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="133a7-130">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="133a7-131">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="133a7-131">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


