---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625033"
---
# <span data-ttu-id="4d269-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="4d269-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="4d269-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4d269-102">SYNOPSIS</span></span>
<span data-ttu-id="4d269-103">下載備份電子倉庫的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="4d269-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d269-104">句法</span><span class="sxs-lookup"><span data-stu-id="4d269-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d269-105">說明</span><span class="sxs-lookup"><span data-stu-id="4d269-105">DESCRIPTION</span></span>
<span data-ttu-id="4d269-106">**AzureRmBackupVaultCredentials** Cmdlet 會下載 Azure 備份電子倉庫的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="4d269-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="4d269-107">[備份] 使用保存庫認證檔案，將伺服器連線至 Azure 備份電子倉庫並進行註冊。</span><span class="sxs-lookup"><span data-stu-id="4d269-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="4d269-108">您必須先註冊伺服器，才能將備份資料傳送到保存庫。</span><span class="sxs-lookup"><span data-stu-id="4d269-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="4d269-109">示例</span><span class="sxs-lookup"><span data-stu-id="4d269-109">EXAMPLES</span></span>

## <span data-ttu-id="4d269-110">參數</span><span class="sxs-lookup"><span data-stu-id="4d269-110">PARAMETERS</span></span>

### <span data-ttu-id="4d269-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d269-111">-DefaultProfile</span></span>
<span data-ttu-id="4d269-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4d269-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d269-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="4d269-113">-TargetLocation</span></span>
<span data-ttu-id="4d269-114">指定此 Cmdlet 儲存保存庫認證檔案的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="4d269-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d269-115">-保存庫</span><span class="sxs-lookup"><span data-stu-id="4d269-115">-Vault</span></span>
<span data-ttu-id="4d269-116">指定此 Cmdlet 取得保存庫認證檔案的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="4d269-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="4d269-117">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4d269-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d269-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d269-118">CommonParameters</span></span>
<span data-ttu-id="4d269-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4d269-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d269-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4d269-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d269-121">輸入</span><span class="sxs-lookup"><span data-stu-id="4d269-121">INPUTS</span></span>

### <span data-ttu-id="4d269-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="4d269-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="4d269-123">輸出</span><span class="sxs-lookup"><span data-stu-id="4d269-123">OUTPUTS</span></span>

### <span data-ttu-id="4d269-124">字串</span><span class="sxs-lookup"><span data-stu-id="4d269-124">String</span></span>
<span data-ttu-id="4d269-125">這個 Cmdlet 會傳回保存庫認證檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="4d269-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="4d269-126">筆記</span><span class="sxs-lookup"><span data-stu-id="4d269-126">NOTES</span></span>

## <span data-ttu-id="4d269-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="4d269-127">RELATED LINKS</span></span>

[<span data-ttu-id="4d269-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="4d269-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


