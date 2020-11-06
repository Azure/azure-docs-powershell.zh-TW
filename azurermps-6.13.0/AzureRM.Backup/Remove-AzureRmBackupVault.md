---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 883c4a9892f4525b15369dbb1c3ed6134eb29f00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447486"
---
# <span data-ttu-id="85089-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="85089-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="85089-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85089-102">SYNOPSIS</span></span>
<span data-ttu-id="85089-103">刪除備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="85089-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85089-104">句法</span><span class="sxs-lookup"><span data-stu-id="85089-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85089-105">說明</span><span class="sxs-lookup"><span data-stu-id="85089-105">DESCRIPTION</span></span>
<span data-ttu-id="85089-106">**AzureRmBackupVault** Cmdlet 會刪除 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="85089-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>
<span data-ttu-id="85089-107">您可以刪除備份保存庫之前，必須先清空該檔案。</span><span class="sxs-lookup"><span data-stu-id="85089-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="85089-108">使用 **AzureRmBackupContainer** Cmdlet，將基礎結構從保存庫中) 虛擬機器備份資料的服務 (IaaS 中移除。</span><span class="sxs-lookup"><span data-stu-id="85089-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="85089-109">使用 **Delete-RegisteredServer** Cmdlet 來移除其他已註冊的伺服器和備份資料。</span><span class="sxs-lookup"><span data-stu-id="85089-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="85089-110">示例</span><span class="sxs-lookup"><span data-stu-id="85089-110">EXAMPLES</span></span>

### <span data-ttu-id="85089-111">範例1：刪除 Azure 備份電子倉庫</span><span class="sxs-lookup"><span data-stu-id="85089-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="85089-112">此命令會使用 **AzureRmBackupVault** Cmdlet 取得名為 Vault03 的 Azure 備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="85089-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="85089-113">命令會使用管線運算子，將該電子倉庫傳送至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85089-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="85089-114">目前的 Cmdlet 會移除該保存庫。</span><span class="sxs-lookup"><span data-stu-id="85089-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="85089-115">參數</span><span class="sxs-lookup"><span data-stu-id="85089-115">PARAMETERS</span></span>

### <span data-ttu-id="85089-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85089-116">-DefaultProfile</span></span>
<span data-ttu-id="85089-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="85089-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85089-118">-Force</span><span class="sxs-lookup"><span data-stu-id="85089-118">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85089-119">-保存庫</span><span class="sxs-lookup"><span data-stu-id="85089-119">-Vault</span></span>
<span data-ttu-id="85089-120">指定此 Cmdlet 移除的備份保存庫。</span><span class="sxs-lookup"><span data-stu-id="85089-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="85089-121">若要取得 **AzureRmBackupVault** ，請使用 Get-AzureRmBackupVault Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85089-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="85089-122">-確認</span><span class="sxs-lookup"><span data-stu-id="85089-122">-Confirm</span></span>
<span data-ttu-id="85089-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85089-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85089-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85089-124">-WhatIf</span></span>
<span data-ttu-id="85089-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85089-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85089-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85089-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85089-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85089-127">CommonParameters</span></span>
<span data-ttu-id="85089-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85089-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85089-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85089-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85089-130">輸入</span><span class="sxs-lookup"><span data-stu-id="85089-130">INPUTS</span></span>

### <span data-ttu-id="85089-131">AzureRMBackupVault 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="85089-131">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="85089-132">參數：保存庫 (ByValue) </span><span class="sxs-lookup"><span data-stu-id="85089-132">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="85089-133">輸出</span><span class="sxs-lookup"><span data-stu-id="85089-133">OUTPUTS</span></span>

### <span data-ttu-id="85089-134">System.void</span><span class="sxs-lookup"><span data-stu-id="85089-134">System.Void</span></span>

## <span data-ttu-id="85089-135">筆記</span><span class="sxs-lookup"><span data-stu-id="85089-135">NOTES</span></span>
* <span data-ttu-id="85089-136">所有</span><span class="sxs-lookup"><span data-stu-id="85089-136">None</span></span>

## <span data-ttu-id="85089-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="85089-137">RELATED LINKS</span></span>

[<span data-ttu-id="85089-138">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="85089-138">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="85089-139">新-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="85089-139">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="85089-140">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="85089-140">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


