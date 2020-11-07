---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F83D698B-DC48-4ACD-AD2E-4AAECBDA196B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc8081c9f81305b96b1ac227b9766352ce94b06
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967530"
---
# <span data-ttu-id="5274e-101">Restart-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="5274e-101">Restart-AzureRemoteAppVM</span></span>

## <span data-ttu-id="5274e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5274e-102">SYNOPSIS</span></span>
<span data-ttu-id="5274e-103">重新開機 Azure RemoteApp 集合中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5274e-103">Restarts a virtual machine in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5274e-104">句法</span><span class="sxs-lookup"><span data-stu-id="5274e-104">SYNTAX</span></span>

```
Restart-AzureRemoteAppVM -CollectionName <String> -UserUpn <String> [-LogoffMessage <String>]
 [-LogoffWaitSeconds <Int32>] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5274e-105">說明</span><span class="sxs-lookup"><span data-stu-id="5274e-105">DESCRIPTION</span></span>
<span data-ttu-id="5274e-106">**Restart AzureRemoteAppVM** Cmdlet 會在已連接指定使用者的 Azure RemoteApp 集合中重新開機虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5274e-106">The **Restart-AzureRemoteAppVM** cmdlet restarts a virtual machine in an Azure RemoteApp collection on which the specified user is connected.</span></span>

## <span data-ttu-id="5274e-107">示例</span><span class="sxs-lookup"><span data-stu-id="5274e-107">EXAMPLES</span></span>

### <span data-ttu-id="5274e-108">範例1：重新開機虛擬機器</span><span class="sxs-lookup"><span data-stu-id="5274e-108">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRemoteAppVM -CollectionName "ContosoVNet" -UserUPN "PattiFuller@contoso.com"
```

<span data-ttu-id="5274e-109">這個命令會重新開機 Azure RemoteApp 集合（名為 Contoso）中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5274e-109">This command restarts a virtual machine in an Azure RemoteApp collection named Contoso.</span></span>
<span data-ttu-id="5274e-110">使用者已 PattiFuller@contoso.com 連線至包含此虛擬機器的集合。</span><span class="sxs-lookup"><span data-stu-id="5274e-110">The user PattiFuller@contoso.com is connected to the collection which contains this virtual machine.</span></span>

## <span data-ttu-id="5274e-111">參數</span><span class="sxs-lookup"><span data-stu-id="5274e-111">PARAMETERS</span></span>

### <span data-ttu-id="5274e-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5274e-112">-CollectionName</span></span>
<span data-ttu-id="5274e-113">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="5274e-113">Specifies the name of an Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="5274e-114">-LogoffMessage</span><span class="sxs-lookup"><span data-stu-id="5274e-114">-LogoffMessage</span></span>
<span data-ttu-id="5274e-115">指定在此 Cmdlet 登出前，向連線至虛擬機器的使用者顯示的警告訊息。</span><span class="sxs-lookup"><span data-stu-id="5274e-115">Specifies a warning message shown to users connected to the virtual machine before this cmdlet logs them off.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5274e-116">-LogoffWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="5274e-116">-LogoffWaitSeconds</span></span>
<span data-ttu-id="5274e-117">指定此指令在登出使用者之前要等待多長時間。</span><span class="sxs-lookup"><span data-stu-id="5274e-117">Specifies how long this cmdlet waits before it logs users off.</span></span>
<span data-ttu-id="5274e-118">預設值為60秒。</span><span class="sxs-lookup"><span data-stu-id="5274e-118">The default value is 60 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5274e-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5274e-119">-Profile</span></span>
<span data-ttu-id="5274e-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5274e-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5274e-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5274e-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5274e-122">-UserUpn</span><span class="sxs-lookup"><span data-stu-id="5274e-122">-UserUpn</span></span>
<span data-ttu-id="5274e-123">指定此 Cmdlet 重新開機虛擬機器之使用者的使用者主要名稱 (UPN) 。</span><span class="sxs-lookup"><span data-stu-id="5274e-123">Specifies the user principal name (UPN) of the user for whom this cmdlet restarts the virtual machine.</span></span>
<span data-ttu-id="5274e-124">若要在集合和連線的 Upn 中取得虛擬機器，請使用 **AzureRemoteAppVM** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5274e-124">To obtain virtual machines in the collection and connected UPNs, use the **Get-AzureRemoteAppVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5274e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="5274e-125">-Confirm</span></span>
<span data-ttu-id="5274e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5274e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5274e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5274e-127">-WhatIf</span></span>
<span data-ttu-id="5274e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5274e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5274e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5274e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5274e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5274e-130">CommonParameters</span></span>
<span data-ttu-id="5274e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5274e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5274e-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5274e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5274e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="5274e-133">INPUTS</span></span>

## <span data-ttu-id="5274e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5274e-134">OUTPUTS</span></span>

## <span data-ttu-id="5274e-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5274e-135">NOTES</span></span>

## <span data-ttu-id="5274e-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5274e-136">RELATED LINKS</span></span>

[<span data-ttu-id="5274e-137">AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="5274e-137">Get-AzureRemoteAppVM</span></span>](./Get-AzureRemoteAppVM.md)


