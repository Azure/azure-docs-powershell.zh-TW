---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: D40937C2-9BF7-4371-A64C-B44F5B6B895E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c9882e805504b2e3b2e4f4ebbe661268b2327a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968017"
---
# <span data-ttu-id="a5920-101">Get-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="a5920-101">Get-AzureRemoteAppVM</span></span>

## <span data-ttu-id="a5920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5920-102">SYNOPSIS</span></span>
<span data-ttu-id="a5920-103">取得 Azure RemoteApp 集合中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5920-103">Gets the virtual machines in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="a5920-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5920-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVM -CollectionName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5920-105">說明</span><span class="sxs-lookup"><span data-stu-id="a5920-105">DESCRIPTION</span></span>
<span data-ttu-id="a5920-106">**AzureRemoteAppVM** Cmdlet 會取得在 Azure RemoteApp 集合下建立的虛擬機器，以進行會話託管。</span><span class="sxs-lookup"><span data-stu-id="a5920-106">The **Get-AzureRemoteAppVM** cmdlet gets the virtual machines created under an Azure RemoteApp collection for session hosting.</span></span>

## <span data-ttu-id="a5920-107">示例</span><span class="sxs-lookup"><span data-stu-id="a5920-107">EXAMPLES</span></span>

### <span data-ttu-id="a5920-108">範例1：顯示集合中的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5920-108">Example 1: Display the virtual machines in a collection</span></span>
```
PS C:\> Get-AzureRemoteAppVM -CollectionName "Contoso"
```

<span data-ttu-id="a5920-109">這個命令會顯示用於在名為 Contoso 的 Azure RemoteApp 集合中裝載之會話的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5920-109">This command displays the virtual machines used for session hosting in an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="a5920-110">參數</span><span class="sxs-lookup"><span data-stu-id="a5920-110">PARAMETERS</span></span>

### <span data-ttu-id="a5920-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="a5920-111">-CollectionName</span></span>
<span data-ttu-id="a5920-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5920-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="a5920-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a5920-113">-Profile</span></span>
<span data-ttu-id="a5920-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a5920-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5920-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a5920-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5920-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5920-116">CommonParameters</span></span>
<span data-ttu-id="a5920-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5920-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5920-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5920-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5920-119">輸入</span><span class="sxs-lookup"><span data-stu-id="a5920-119">INPUTS</span></span>

## <span data-ttu-id="a5920-120">輸出</span><span class="sxs-lookup"><span data-stu-id="a5920-120">OUTPUTS</span></span>

## <span data-ttu-id="a5920-121">筆記</span><span class="sxs-lookup"><span data-stu-id="a5920-121">NOTES</span></span>

## <span data-ttu-id="a5920-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5920-122">RELATED LINKS</span></span>

[<span data-ttu-id="a5920-123">重新開機-AzureRemoteAppVM</span><span class="sxs-lookup"><span data-stu-id="a5920-123">Restart-AzureRemoteAppVM</span></span>](./Restart-AzureRemoteAppVM.md)


