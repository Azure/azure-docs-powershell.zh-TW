---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967954"
---
# <span data-ttu-id="8c060-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8c060-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="8c060-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c060-102">SYNOPSIS</span></span>
<span data-ttu-id="8c060-103">取得雲端 VM 角色大小設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8c060-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="8c060-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c060-104">SYNTAX</span></span>

### <span data-ttu-id="8c060-105">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="8c060-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8c060-106">FromName</span><span class="sxs-lookup"><span data-stu-id="8c060-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8c060-107">說明</span><span class="sxs-lookup"><span data-stu-id="8c060-107">DESCRIPTION</span></span>
<span data-ttu-id="8c060-108">**WAPackCloudVMRoleSizeProfile** Cmdlet 會取得虛擬機器的雲端 VM 角色大小設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="8c060-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="8c060-109">示例</span><span class="sxs-lookup"><span data-stu-id="8c060-109">EXAMPLES</span></span>

### <span data-ttu-id="8c060-110">範例1：使用名稱取得雲端 VM 角色大小設定檔</span><span class="sxs-lookup"><span data-stu-id="8c060-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="8c060-111">這個命令會取得名為 Small 的大小設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c060-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="8c060-112">範例2：取得所有雲端 VM 角色大小設定檔</span><span class="sxs-lookup"><span data-stu-id="8c060-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="8c060-113">這個命令會取得所有大小設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c060-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="8c060-114">參數</span><span class="sxs-lookup"><span data-stu-id="8c060-114">PARAMETERS</span></span>

### <span data-ttu-id="8c060-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="8c060-115">-Name</span></span>
<span data-ttu-id="8c060-116">指定雲端 VM 角色大小設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c060-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c060-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8c060-117">-Profile</span></span>
<span data-ttu-id="8c060-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8c060-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8c060-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8c060-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8c060-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c060-120">CommonParameters</span></span>
<span data-ttu-id="8c060-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c060-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c060-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8c060-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c060-123">輸入</span><span class="sxs-lookup"><span data-stu-id="8c060-123">INPUTS</span></span>

## <span data-ttu-id="8c060-124">輸出</span><span class="sxs-lookup"><span data-stu-id="8c060-124">OUTPUTS</span></span>

## <span data-ttu-id="8c060-125">筆記</span><span class="sxs-lookup"><span data-stu-id="8c060-125">NOTES</span></span>

## <span data-ttu-id="8c060-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c060-126">RELATED LINKS</span></span>

[<span data-ttu-id="8c060-127">WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8c060-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


