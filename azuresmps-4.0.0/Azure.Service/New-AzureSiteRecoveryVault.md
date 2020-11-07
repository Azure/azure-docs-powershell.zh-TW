---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: FD43AFDA-E37D-4B5E-8EB5-CC2CF1E36AFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: ea09f45de760de7ff02a768094c6f98c3f2a0643
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967420"
---
# <span data-ttu-id="a531b-101">New-AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a531b-101">New-AzureSiteRecoveryVault</span></span>

## <span data-ttu-id="a531b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a531b-102">SYNOPSIS</span></span>
<span data-ttu-id="a531b-103">建立網站復原服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="a531b-103">Creates a Site Recovery services vault.</span></span>

## <span data-ttu-id="a531b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a531b-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryVault -Name <String> -Location <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a531b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a531b-105">DESCRIPTION</span></span>
<span data-ttu-id="a531b-106">**新的-AzureSiteRecoveryVault** Cmdlet 會建立 Azure Site Recovery 服務保存庫。</span><span class="sxs-lookup"><span data-stu-id="a531b-106">The **New-AzureSiteRecoveryVault** cmdlet creates an Azure Site Recovery services vault.</span></span>

## <span data-ttu-id="a531b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a531b-107">EXAMPLES</span></span>

### <span data-ttu-id="a531b-108">範例1：建立電子倉庫</span><span class="sxs-lookup"><span data-stu-id="a531b-108">Example 1: Create a vault</span></span>
```
PS C:\> New-AzureSiteRecoveryVault -Location "West US" -Name "ContosoVault" 
Response
--------
Vault has been created
```

<span data-ttu-id="a531b-109">這個命令會在 [西部美國] 位置建立一個名為 ContosoVault 的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="a531b-109">This command creates a vault named ContosoVault in the West US location.</span></span>

## <span data-ttu-id="a531b-110">參數</span><span class="sxs-lookup"><span data-stu-id="a531b-110">PARAMETERS</span></span>

### <span data-ttu-id="a531b-111">-位置</span><span class="sxs-lookup"><span data-stu-id="a531b-111">-Location</span></span>
<span data-ttu-id="a531b-112">指定地理位置。</span><span class="sxs-lookup"><span data-stu-id="a531b-112">Specifies the geographical location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a531b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a531b-113">-Name</span></span>
<span data-ttu-id="a531b-114">指定保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a531b-114">Specifies the name of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a531b-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a531b-115">-Profile</span></span>
<span data-ttu-id="a531b-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a531b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a531b-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a531b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a531b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a531b-118">CommonParameters</span></span>
<span data-ttu-id="a531b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a531b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a531b-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a531b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a531b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a531b-121">INPUTS</span></span>

## <span data-ttu-id="a531b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="a531b-122">OUTPUTS</span></span>

## <span data-ttu-id="a531b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="a531b-123">NOTES</span></span>

## <span data-ttu-id="a531b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="a531b-124">RELATED LINKS</span></span>

[<span data-ttu-id="a531b-125">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="a531b-125">Get-AzureSiteRecoveryVault</span></span>](./Get-AzureSiteRecoveryVault.md)


