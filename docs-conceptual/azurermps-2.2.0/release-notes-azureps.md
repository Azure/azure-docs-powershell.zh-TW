---
title: Azure PowerShell 變更記錄 | Microsoft Docs
description: 這是在最新版中對 Azure powershell 所做的變更歷程記錄。
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: a00bc2f13117f1b07f0dcc5808eddbabe1df940f
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821661"
---
# <a name="release-notes"></a><span data-ttu-id="54036-103">版本資訊</span><span class="sxs-lookup"><span data-stu-id="54036-103">Release notes</span></span>

<span data-ttu-id="54036-104">這是此版本中對 Azure PowerShell 所做的變更清單。</span><span class="sxs-lookup"><span data-stu-id="54036-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-220"></a><span data-ttu-id="54036-105">2.2.0 版</span><span class="sxs-lookup"><span data-stu-id="54036-105">Version 2.2.0</span></span>
* <span data-ttu-id="54036-106">計算</span><span class="sxs-lookup"><span data-stu-id="54036-106">Compute</span></span>
  - <span data-ttu-id="54036-107">新增從 AzureDiskEncryptionForLinux 擴充查詢加密狀態的支援</span><span class="sxs-lookup"><span data-stu-id="54036-107">Add support for querying encryption status from the AzureDiskEncryptionForLinux extension</span></span>
* <span data-ttu-id="54036-108">DataFactory</span><span class="sxs-lookup"><span data-stu-id="54036-108">DataFactory</span></span>
  - <span data-ttu-id="54036-109">已新增 Cmdlet 以供列出活動時段</span><span class="sxs-lookup"><span data-stu-id="54036-109">Added new cmdlet for listing activity windows</span></span>
    + <span data-ttu-id="54036-110">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="54036-110">Get-AzureRmDataFactoryActivityWindow</span></span>
* <span data-ttu-id="54036-111">DataLake</span><span class="sxs-lookup"><span data-stu-id="54036-111">DataLake</span></span>
  - <span data-ttu-id="54036-112">已將參數 `Host` 變更為 `DatabaseHost` 並將別名新增至 `Host`</span><span class="sxs-lookup"><span data-stu-id="54036-112">Changed parameter `Host` to `DatabaseHost` and added alias to `Host`</span></span>
    + <span data-ttu-id="54036-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="54036-113">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
    + <span data-ttu-id="54036-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="54036-114">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>
  - <span data-ttu-id="54036-115">新增 ACL 和預設 ACL 移除的支援</span><span class="sxs-lookup"><span data-stu-id="54036-115">Add support for ACL and Default ACL removal</span></span>
  - <span data-ttu-id="54036-116">新增取得及設定檔案和資料夾之未命名權限的支援</span><span class="sxs-lookup"><span data-stu-id="54036-116">Add support for getting and setting unnamed permissions on files and folders</span></span>
* <span data-ttu-id="54036-117">KeyVault</span><span class="sxs-lookup"><span data-stu-id="54036-117">KeyVault</span></span>
  - <span data-ttu-id="54036-118">新增憑證的支援</span><span class="sxs-lookup"><span data-stu-id="54036-118">Add support for certificates</span></span>
    + <span data-ttu-id="54036-119">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54036-119">Add-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="54036-120">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="54036-120">Add-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="54036-121">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54036-121">Get-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="54036-122">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="54036-122">Get-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="54036-123">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="54036-123">Get-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="54036-124">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="54036-124">Get-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="54036-125">Get-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="54036-125">Get-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="54036-126">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54036-126">Import-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="54036-127">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="54036-127">New-AzureKeyVaultCertificateAdministratorDetails</span></span>
    + <span data-ttu-id="54036-128">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="54036-128">New-AzureKeyVaultCertificateOrganizationDetails</span></span>
    + <span data-ttu-id="54036-129">New-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="54036-129">New-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="54036-130">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="54036-130">Remove-AzureKeyVaultCertificate</span></span>
    + <span data-ttu-id="54036-131">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="54036-131">Remove-AzureKeyVaultCertificateContact</span></span>
    + <span data-ttu-id="54036-132">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="54036-132">Remove-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="54036-133">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="54036-133">Remove-AzureKeyVaultCertificateOperation</span></span>
    + <span data-ttu-id="54036-134">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="54036-134">Set-AzureKeyVaultCertificateAttribute</span></span>
    + <span data-ttu-id="54036-135">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="54036-135">Set-AzureKeyVaultCertificateIssuer</span></span>
    + <span data-ttu-id="54036-136">Set-AzureKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="54036-136">Set-AzureKeyVaultCertificatePolicy</span></span>
    + <span data-ttu-id="54036-137">Stop-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="54036-137">Stop-AzureKeyVaultCertificateOperation</span></span>
* <span data-ttu-id="54036-138">網路</span><span class="sxs-lookup"><span data-stu-id="54036-138">Network</span></span>

  - <span data-ttu-id="54036-139">新增網路介面的切換參數來啟用/停用加速網路 +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="54036-139">New switch parameter added for network interface to enable/disable accelerated networking +New-AzureRmNetworkInterface -EnableAcceleratedNetworking</span></span>
  - <span data-ttu-id="54036-140">啟用主動-主動閘道功能 PowerShell Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54036-140">Enable Active-Active gateway feature PowerShell cmdlets</span></span>
    + <span data-ttu-id="54036-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="54036-141">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
    + <span data-ttu-id="54036-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="54036-142">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="54036-143">已新增 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54036-143">Added new cmdlet</span></span>
    + <span data-ttu-id="54036-144">Test-AzureRmPrivateIpAddressAvailability</span><span class="sxs-lookup"><span data-stu-id="54036-144">Test-AzureRmPrivateIpAddressAvailability</span></span>
* <span data-ttu-id="54036-145">資源</span><span class="sxs-lookup"><span data-stu-id="54036-145">Resources</span></span>
  - <span data-ttu-id="54036-146">支援提供者和資源 Cmdlet 的區域</span><span class="sxs-lookup"><span data-stu-id="54036-146">Support zones in provider and resource cmdlets</span></span>
    + <span data-ttu-id="54036-147">Get-AzureRmProvider</span><span class="sxs-lookup"><span data-stu-id="54036-147">Get-AzureRmProvider</span></span>
    + <span data-ttu-id="54036-148">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="54036-148">New-AzureRmResource</span></span>
    + <span data-ttu-id="54036-149">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="54036-149">Set-AzureRmResource</span></span>
* <span data-ttu-id="54036-150">Sql</span><span class="sxs-lookup"><span data-stu-id="54036-150">Sql</span></span>
  - <span data-ttu-id="54036-151">已在伺服器層級新增用於 Azure SQL 威脅偵測原則管理的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54036-151">Added new cmdlets for Azure SQL threat detection policy management at server level</span></span>
    + <span data-ttu-id="54036-152">Get-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-152">Get-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="54036-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-153">Remove-AzureRmSqlServerThreatDetectionPolicy</span></span>
    + <span data-ttu-id="54036-154">Set-AzureRmSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-154">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
  - <span data-ttu-id="54036-155">已新增 Cmdlet 來支援為 Sql Azure DataWarehouse 啟用/停用 GeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-155">Added new cmdlets to support enabling/disabling GeoBackupPolicy for Sql Azure DataWarehouses</span></span>
    + <span data-ttu-id="54036-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-156">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
    + <span data-ttu-id="54036-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="54036-157">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>
  - <span data-ttu-id="54036-158">已新增 Azure Sql Advisor 和建議動作 API 的 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54036-158">Added new cmdlets for Azure Sql Advisors and Recommended Actions APIs</span></span>
    + <span data-ttu-id="54036-159">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="54036-159">Get-AzureRmSqlDatabaseAdvisor</span></span>
    + <span data-ttu-id="54036-160">Get-AzureRmSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="54036-160">Get-AzureRmSqlElasticPoolAdvisor</span></span>
    + <span data-ttu-id="54036-161">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="54036-161">Get-AzureRmSqlServerAdvisor</span></span>
    + <span data-ttu-id="54036-162">Get-AzureRmSqlDatabaseRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="54036-162">Get-AzureRmSqlDatabaseRecommendedActions</span></span>
    + <span data-ttu-id="54036-163">Get-AzureRmSqlElasticPoolRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="54036-163">Get-AzureRmSqlElasticPoolRecommendedActions</span></span>
    + <span data-ttu-id="54036-164">Get-AzureRmSqlServerRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="54036-164">Get-AzureRmSqlServerRecommendedActions</span></span>
    + <span data-ttu-id="54036-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="54036-165">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="54036-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="54036-166">Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="54036-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="54036-167">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>
    + <span data-ttu-id="54036-168">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="54036-168">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>
    + <span data-ttu-id="54036-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="54036-169">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>
    + <span data-ttu-id="54036-170">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="54036-170">Set-AzureRmSqlServerRecommendedActionState</span></span>
