---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: 6ee9e3062108049e517dbea09573af7905dd54d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624919"
---
# <span data-ttu-id="2113f-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="2113f-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="2113f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2113f-102">SYNOPSIS</span></span>
<span data-ttu-id="2113f-103">下載備份電子倉庫的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="2113f-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2113f-104">句法</span><span class="sxs-lookup"><span data-stu-id="2113f-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2113f-105">說明</span><span class="sxs-lookup"><span data-stu-id="2113f-105">DESCRIPTION</span></span>
<span data-ttu-id="2113f-106">**AzureRmBackupVaultCredentials** Cmdlet 會下載 Azure 備份電子倉庫的保存庫認證檔案。</span><span class="sxs-lookup"><span data-stu-id="2113f-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>
<span data-ttu-id="2113f-107">[備份] 使用保存庫認證檔案，將伺服器連線至 Azure 備份電子倉庫並進行註冊。</span><span class="sxs-lookup"><span data-stu-id="2113f-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="2113f-108">您必須先註冊伺服器，才能將備份資料傳送到保存庫。</span><span class="sxs-lookup"><span data-stu-id="2113f-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="2113f-109">示例</span><span class="sxs-lookup"><span data-stu-id="2113f-109">EXAMPLES</span></span>

## <span data-ttu-id="2113f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2113f-110">PARAMETERS</span></span>

### <span data-ttu-id="2113f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2113f-111">-DefaultProfile</span></span>
<span data-ttu-id="2113f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2113f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2113f-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="2113f-113">-TargetLocation</span></span>
<span data-ttu-id="2113f-114">指定此 Cmdlet 儲存保存庫認證檔案的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="2113f-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2113f-115">-保存庫</span><span class="sxs-lookup"><span data-stu-id="2113f-115">-Vault</span></span>
<span data-ttu-id="2113f-116">指定此 Cmdlet 取得保存庫認證檔案的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="2113f-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="2113f-117">若要取得 **AzureRmBackupVault** 物件，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2113f-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2113f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2113f-118">CommonParameters</span></span>
<span data-ttu-id="2113f-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2113f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2113f-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2113f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2113f-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2113f-121">INPUTS</span></span>

### <span data-ttu-id="2113f-122">AzureRMBackupVault 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="2113f-122">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="2113f-123">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2113f-123">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="2113f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2113f-124">OUTPUTS</span></span>

### <span data-ttu-id="2113f-125">System.object</span><span class="sxs-lookup"><span data-stu-id="2113f-125">System.String</span></span>
<span data-ttu-id="2113f-126">這個 Cmdlet 會傳回保存庫認證檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2113f-126">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="2113f-127">筆記</span><span class="sxs-lookup"><span data-stu-id="2113f-127">NOTES</span></span>

## <span data-ttu-id="2113f-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="2113f-128">RELATED LINKS</span></span>

[<span data-ttu-id="2113f-129">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="2113f-129">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


