---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967149"
---
# <span data-ttu-id="ede11-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ede11-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="ede11-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ede11-102">SYNOPSIS</span></span>
<span data-ttu-id="ede11-103">移除與已不存在之 Azure RemoteApp 虛擬機器相關聯的 Azure Active Directory 中的物件。</span><span class="sxs-lookup"><span data-stu-id="ede11-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="ede11-104">句法</span><span class="sxs-lookup"><span data-stu-id="ede11-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede11-105">說明</span><span class="sxs-lookup"><span data-stu-id="ede11-105">DESCRIPTION</span></span>
<span data-ttu-id="ede11-106">**Clear AzureRemoteAppVmStaleAdObject** Cmdlet 會移除與已不存在之 azure RemoteApp 虛擬機器相關聯的 Azure Active Directory 中的物件。</span><span class="sxs-lookup"><span data-stu-id="ede11-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="ede11-107">您必須使用具有移除 Azure Active Directory 物件許可權的認證。</span><span class="sxs-lookup"><span data-stu-id="ede11-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="ede11-108">如果您指定 *詳細* 的常見參數，這個 Cmdlet 會顯示它刪除的每個物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede11-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="ede11-109">示例</span><span class="sxs-lookup"><span data-stu-id="ede11-109">EXAMPLES</span></span>

### <span data-ttu-id="ede11-110">範例1：清除集合的過時物件</span><span class="sxs-lookup"><span data-stu-id="ede11-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="ede11-111">第一個命令會使用 [ **取得認證** ] 提示您輸入使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="ede11-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="ede11-112">該命令會將結果儲存在 $AdminCredentials 變數中。</span><span class="sxs-lookup"><span data-stu-id="ede11-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="ede11-113">第二個命令會清除名為 Contoso 的集合的過時物件。</span><span class="sxs-lookup"><span data-stu-id="ede11-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="ede11-114">此命令使用 $AdminCredentials 變數中儲存的認證。</span><span class="sxs-lookup"><span data-stu-id="ede11-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="ede11-115">為了讓命令成功，這些認證必須具有適當的許可權。</span><span class="sxs-lookup"><span data-stu-id="ede11-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="ede11-116">參數</span><span class="sxs-lookup"><span data-stu-id="ede11-116">PARAMETERS</span></span>

### <span data-ttu-id="ede11-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ede11-117">-CollectionName</span></span>
<span data-ttu-id="ede11-118">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede11-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ede11-119">-認證</span><span class="sxs-lookup"><span data-stu-id="ede11-119">-Credential</span></span>
<span data-ttu-id="ede11-120">指定有權執行此動作的認證。</span><span class="sxs-lookup"><span data-stu-id="ede11-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="ede11-121">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ede11-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="ede11-122">如果您沒有指定此參數，這個 Cmdlet 會使用目前的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="ede11-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="ede11-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ede11-123">-Profile</span></span>
<span data-ttu-id="ede11-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ede11-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ede11-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ede11-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ede11-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ede11-126">-Confirm</span></span>
<span data-ttu-id="ede11-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ede11-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede11-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede11-128">-WhatIf</span></span>
<span data-ttu-id="ede11-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ede11-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede11-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ede11-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede11-131">CommonParameters</span></span>
<span data-ttu-id="ede11-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ede11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede11-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ede11-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede11-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ede11-134">INPUTS</span></span>

## <span data-ttu-id="ede11-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ede11-135">OUTPUTS</span></span>

## <span data-ttu-id="ede11-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ede11-136">NOTES</span></span>

## <span data-ttu-id="ede11-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ede11-137">RELATED LINKS</span></span>

[<span data-ttu-id="ede11-138">AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ede11-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


