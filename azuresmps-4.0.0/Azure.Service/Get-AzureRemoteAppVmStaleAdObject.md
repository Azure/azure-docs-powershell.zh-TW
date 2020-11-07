---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967076"
---
# <span data-ttu-id="39972-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="39972-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="39972-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39972-102">SYNOPSIS</span></span>
<span data-ttu-id="39972-103">在 Azure Active Directory 中取得已不再存在之 Azure RemoteApp 虛擬機器相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="39972-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="39972-104">句法</span><span class="sxs-lookup"><span data-stu-id="39972-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39972-105">說明</span><span class="sxs-lookup"><span data-stu-id="39972-105">DESCRIPTION</span></span>
<span data-ttu-id="39972-106">**AzureRemoteAppVmStaleAdObject** Cmdlet 會取得 Azure Active Directory 中與已不存在之 azure RemoteApp 虛擬機器相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="39972-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="39972-107">這個 Cmdlet 會顯示它所取得的每個物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="39972-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="39972-108">示例</span><span class="sxs-lookup"><span data-stu-id="39972-108">EXAMPLES</span></span>

### <span data-ttu-id="39972-109">範例1：取得集合的陳舊物件</span><span class="sxs-lookup"><span data-stu-id="39972-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="39972-110">第二個命令會取得名為 Contoso 的集合的陳舊物件。</span><span class="sxs-lookup"><span data-stu-id="39972-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="39972-111">參數</span><span class="sxs-lookup"><span data-stu-id="39972-111">PARAMETERS</span></span>

### <span data-ttu-id="39972-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="39972-112">-CollectionName</span></span>
<span data-ttu-id="39972-113">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="39972-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39972-114">-認證</span><span class="sxs-lookup"><span data-stu-id="39972-114">-Credential</span></span>
<span data-ttu-id="39972-115">指定有權執行此動作的認證。</span><span class="sxs-lookup"><span data-stu-id="39972-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="39972-116">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39972-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="39972-117">如果您沒有指定此參數，這個 Cmdlet 會使用目前的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="39972-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39972-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="39972-118">-Profile</span></span>
<span data-ttu-id="39972-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="39972-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39972-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="39972-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39972-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39972-121">CommonParameters</span></span>
<span data-ttu-id="39972-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39972-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39972-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39972-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39972-124">輸入</span><span class="sxs-lookup"><span data-stu-id="39972-124">INPUTS</span></span>

## <span data-ttu-id="39972-125">輸出</span><span class="sxs-lookup"><span data-stu-id="39972-125">OUTPUTS</span></span>

### <span data-ttu-id="39972-126">字串</span><span class="sxs-lookup"><span data-stu-id="39972-126">String</span></span>

## <span data-ttu-id="39972-127">筆記</span><span class="sxs-lookup"><span data-stu-id="39972-127">NOTES</span></span>

## <span data-ttu-id="39972-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="39972-128">RELATED LINKS</span></span>

[<span data-ttu-id="39972-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="39972-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


